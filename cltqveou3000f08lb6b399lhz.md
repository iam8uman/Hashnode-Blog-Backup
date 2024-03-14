---
title: "Wisock server socket:"
datePublished: Thu Mar 14 2024 06:50:07 GMT+0000 (Coordinated Universal Time)
cuid: cltqveou3000f08lb6b399lhz
slug: wisock-server-socket
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/yLDabpoCL3s/upload/bb41d42c37feb21a69f3e881cf2c4823.jpeg
tags: server, server-side-rendering

---

Here's a simplified explanation of setting up a server socket:

1. **Get Address Info**: Use the `getaddrinfo` function to determine the values for the `sockaddr` structure. This includes specifying the address family (`AF_INET` for IPv4), socket type (`SOCK_STREAM` for stream sockets), and protocol (`IPPROTO_TCP` for TCP). The `AI_PASSIVE` flag indicates that the socket will be used by a server, and the port number (`27015` in this case) is specified.
    

```c
#define DEFAULT_PORT "27015"
struct addrinfo *result = NULL, *ptr = NULL, hints;
ZeroMemory(&hints, sizeof(hints));
hints.ai_family = AF_INET;
hints.ai_socktype = SOCK_STREAM;
hints.ai_protocol = IPPROTO_TCP;
hints.ai_flags = AI_PASSIVE;

iResult = getaddrinfo(NULL, DEFAULT_PORT, &hints, &result);
if (iResult != 0) {
    printf("getaddrinfo failed: %d\n", iResult);
    WSACleanup();
    return 1;
}
```

2. **Create Socket**: Create a `SOCKET` object called `ListenSocket` for the server to listen for client connections.
    

```c
SOCKET ListenSocket = INVALID_SOCKET;
ListenSocket = socket(result->ai_family, result->ai_socktype, result->ai_protocol);
if (ListenSocket == INVALID_SOCKET) {
    printf("Error at socket(): %ld\n", WSAGetLastError());
    freeaddrinfo(result);
    WSACleanup();
    return 1;
}
```

3. **Bind Socket**: Bind the socket to the IP address and port number specified in the `sockaddr` structure returned by `getaddrinfo`.
    

```c
iResult = bind(ListenSocket, result->ai_addr, (int)result->ai_addrlen);
if (iResult == SOCKET_ERROR) {
    printf("bind failed with error: %d\n", WSAGetLastError());
    freeaddrinfo(result);
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```

4. **Listen for Connections**: Use the `listen` function to make the socket listen for incoming connections.
    

```c
if (listen(ListenSocket, SOMAXCONN) == SOCKET_ERROR) {
    printf("Listen failed with error: %ld\n", WSAGetLastError());
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```

5. **Accept Connection**: Accept incoming connections from clients using the `accept` function.
    

```c
SOCKET ClientSocket = INVALID_SOCKET;
ClientSocket = accept(ListenSocket, NULL, NULL);
if (ClientSocket == INVALID_SOCKET) {
    printf("accept failed: %d\n", WSAGetLastError());
    closesocket(ListenSocket);
    WSACleanup();
    return 1;
}
```

This process sets up the server to accept client connections and handle them accordingly.