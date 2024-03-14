---
title: "Winsock client socket:"
datePublished: Thu Mar 14 2024 06:48:51 GMT+0000 (Coordinated Universal Time)
cuid: cltqvd1m7000m09l7du1lf6v3
slug: winsock-client-socket
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/GC1syEKyWDI/upload/a6ee40b3346fe749b1ce5f9382c3c02d.jpeg
tags: windows, client-server

---

Sure, here's a simplified explanation of setting up a client socket:

1. **Get Address Info**: Use the `getaddrinfo` function to determine the values for the `sockaddr` structure. This includes specifying the address family (`AF_UNSPEC` for unspecified), socket type (`SOCK_STREAM` for stream sockets), and protocol (`IPPROTO_TCP` for TCP). Provide the server's IP address and port number (`27015` in this case) to connect to.
    

```c
#define DEFAULT_PORT "27015"
struct addrinfo *result = NULL, *ptr = NULL, hints;
ZeroMemory(&hints, sizeof(hints));
hints.ai_family = AF_UNSPEC;
hints.ai_socktype = SOCK_STREAM;
hints.ai_protocol = IPPROTO_TCP;

iResult = getaddrinfo(argv[1], DEFAULT_PORT, &hints, &result);
if (iResult != 0) {
    printf("getaddrinfo failed: %d\n", iResult);
    WSACleanup();
    return 1;
}
```

2. **Create Socket**: Create a `SOCKET` object called `ConnectSocket` for the client to connect to the server.
    

```c
SOCKET ConnectSocket = INVALID_SOCKET;
ConnectSocket = socket(result->ai_family, result->ai_socktype, result->ai_protocol);
if (ConnectSocket == INVALID_SOCKET) {
    printf("Error at socket(): %ld\n", WSAGetLastError());
    freeaddrinfo(result);
    WSACleanup();
    return 1;
}
```

3. **Connect to Server**: Use the `connect` function to establish a connection to the server.
    

```c
iResult = connect(ConnectSocket, result->ai_addr, (int)result->ai_addrlen);
if (iResult == SOCKET_ERROR) {
    printf("Unable to connect to server!\n");
    closesocket(ConnectSocket);
    WSACleanup();
    return 1;
}
```

4. **Send and Receive Data**: Use the `send` and `recv` functions to send and receive data to and from the server.
    

```c
// Send data
iResult = send(ConnectSocket, sendbuf, (int)strlen(sendbuf), 0);
if (iResult == SOCKET_ERROR) {
    printf("send failed: %d\n", WSAGetLastError());
    closesocket(ConnectSocket);
    WSACleanup();
    return 1;
}

// Receive data
do {
    iResult = recv(ConnectSocket, recvbuf, recvbuflen, 0);
    if (iResult > 0) {
        printf("Bytes received: %d\n", iResult);
        // Process received data
    } else if (iResult == 0) {
        printf("Connection closed\n");
    } else {
        printf("recv failed: %d\n", WSAGetLastError());
        closesocket(ConnectSocket);
        WSACleanup();
        return 1;
    }
} while (iResult > 0);
```

5. **Disconnect**: Once communication is complete, close the socket and clean up resources.
    

```c
closesocket(ConnectSocket);
WSACleanup();
```

This sets up the client to connect to the server and exchange data with it.