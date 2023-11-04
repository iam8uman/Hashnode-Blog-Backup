---
title: "Appwrite authentication | signup, login, setEmailSession,"
seoTitle: "Appwrite authentication | signup, login, setEmailSession,"
seoDescription: "Appwrite authentication | signup, login, setEmailSession,"
datePublished: Sat Nov 04 2023 18:17:58 GMT+0000 (Coordinated Universal Time)
cuid: clokdao04000009l19n5y5tpb
slug: appwrite-authentication
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1699121699449/80d4ccf7-bac3-4c84-8936-0e99c5761e36.png
tags: authentication, authorization, appwrite, whysumancode, emailsession

---

---

1. ### First, we make a client with API endpoint and projectID like this, and then account.
    

```javascript
import { Client, Account, ID } from "appwrite";

const client = new Client()
    .setEndpoint('https://cloud.appwrite.io/v1') // Your API Endpoint
    .setProject('<PROJECT_ID>');               // Your project ID

const account = new Account(client);
```

---

1. ### Now we first start with signup/ createAccount like this,
    
    Here for signup, we only take `email, password & name` of the user. The unique ID is provided by the appwrite `ID.unique().`
    
    I just logged in a user when she/he immediately signup their account. So that they don't have to enter username and password again. It depends upon your own conditions.
    

```javascript
  async createAccount({ email, password, name }) {
    const userAccount = await this.account.create(
      ID.unique(),
      email,
      password,
      name
    );
    if (userAccount) {
      //call another method or success message
      return this.login({email,password})

    } else {
      return userAccount;
    }
  }
```

---

1. ### Login and EmailSession
    

After logged In you can do whatever you want here I am going to set emailSession for the sake of simplicity.

```javascript
async Login({email, password}){
    try{
 return await this.account.createEmailSession(email, password);
}catch(err){
    console.warn("Error during :: Login :: ", err)
}
}
```

After logged In emailSession is created which keeps track of when the user is logged in or not at any time when we access the user's session.

---