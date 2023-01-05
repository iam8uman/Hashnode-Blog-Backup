# How to install  Xampp Server on Ubuntu all versions-7 step solutions

To Install Xampp server on ubuntu, You can follow these 7 steps :

1. First, go to any web browser and search for download Xampp for linux. (That will take you to the download page)
    
2. Second, Just click on the download button. ( It takes some time to download according to your internet speed)
    
3. After the completion of the download, open the terminal and go to the downloads folder(Or Where you download the xampp).
    
    ```apache
    cd Downloads
    ```
    
4. Run the following command in the same pattern to check file exist or not. If file exists named as " [**xampp-linux-x64-7.3.5.1-installer.run**](http://xampp-linux-x64-7.3.5.1-installer.run) "
    

```apache
ls
```

1. if exists check the permission of that files. (run this command)
    

```apache
ls -al
```

If your xampp file has not 'X' in the permission for eg "**\-rw-rw-r--**" like this, then you have to change the permission of that file.

1. To make the latest XAMPP installation package executable, use the command:
    
    ```apache
    sudo chmod 755 xampp-linux-x64-7.3.5.1-installer.run
    ```
    
    Again check the permission given to the users
    

```apache
ls -al
```

If it has "**\-rwxwxr-x**" the file permission is like "Access guaranteed". You can run this file.

1. Completed the installation process. Now Lunch Setup Wizard. Run this command:
    

```apache
sudo ./xampp-linux-x64-7.3.5.1-installer.run
```

The XAMPP Setup Wizard opens in a new window on top of the terminal that will appear as in the following image:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1672933490888/3bb1d4b1-9e36-4c9e-b11d-ed5e16c79d0e.png align="center")

* Click **Next** and in the following **Select Components** dialogue, choose the components you want to install. We recommend keeping the default settings and continuing with **Next**.
    
* After selecting the components, the setup wizard will show you the location where it will install the software. To proceed, click **Next**.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1672933669248/4dafbeaf-9a94-4ea1-8a9a-7b38f197f9f2.png align="center")
    
* You can deny installing additional software by unchecking the **Learn more about Bitnami for XAMPP** box.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1672933754267/29e6a762-5212-4cdf-afd6-744244bd12a5.png align="center")
    
* Next, the wizard will notify you that it is **ready to install XAMPP** on your system. Click **Next** to start.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1672933846773/210fc251-26f9-43c8-adc6-e0b0a6c4891b.png align="center")
    
* After installing by clicking **Finish** in the previous step, XAMPP launches its control panel which will appear as in the image below.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1672933935066/a7415345-ed64-4dd1-abd9-845ff3f53b6e.png align="center")
    
* Open the **Manage Servers** tab to see all the available services and their status. You can change their status by selecting **Start** or **Stop**.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1672934031148/fa9e3454-3931-4dac-8dbf-e606237bbd29.png align="center")
    

## If you want to run directly with the least command (run this command):

Open the terminal and navigate to the `opt/lampp` directory with the command:

```apache
cd /opt/lampp
```

To lunch xampp run this command and you will get this GUI

```apache
sudo ./manager-linux-x64.run
```

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1672934448643/a62728a8-9762-42a5-86db-4411c2bf1df2.png align="center")

## To Uninstall Xampp

* To uninstall XAMPP, return to the terminal and navigate to the `opt/lampp` directory with the command:
    
    ```apache
    cd /opt/lampp
    ```
    
* Once you are in the appropriate directory, you can uninstall XAMPP by typing the following command:
    
    ```apache
    sudo ./uninstall
    ```
    
* The command will prompt a dialogue box asking you whether you want to uninstall XAMPP and all of its modules. Confirm by clicking **Yes**.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1672934645558/aaa30ee6-40e0-4050-b7ee-1eb493a302c7.png align="center")
    
* After the process is complete, the output will confirm that XAMPP has been uninstalled.
    
* Finally, remove the specified directory with:
    
    ```apache
    sudo rm –r /opt/lamp
    ```
    

### Here You will learn how to install Xampp in ubuntu all versions

> " You can, There you are " Happy face, Happy coder :) @[Suman Sharma](@Me8848You) ❤️