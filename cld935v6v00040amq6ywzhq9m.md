# How to Kill a Process Running on a Specific PORT in Ubuntu || Linux-based OS.

There are various methods to kill a process running on a specific port in Linux. If you are doing some Reactjs & Nodejs projects you will find this kind of error "Something is running at the PORT 8080" like this.

If you Restart your PC and then again open that project you won't find that error. But you can run your project without restarting your PC like this.

### 2 Popular & Easy Methods:

**Method First**: You can execute this command to kill the process using port 3000 or a specific port.

```plaintext
npx kill-port 3000
```

**Method Second**: You can also execute this command to kill the process running on a specific port.

```plaintext
fuser -k 3000/tcp
```

Thumbs up if this information is useful to you.

> "Happy Face,Happy Coder"-Keep Learning