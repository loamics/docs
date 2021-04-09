## V. Connect your local machine to SFTP server

In this tutorial, you'll learn how to connect and use SFTP server hosted on Azure Cloud.

### Using WinSCP
Windows -> Start Menu -> All Programs -> WinSCP:  
![winscp_desktop_open](imgs/winscp_desktop_open.png "")

Create New Site:
① Select New Site.  
② Select SFTP protocol.  
③ Paste the SFTP Enpoint (`sftpUrl`)  
④ Select Port: 22  
⑤ Input User name: `sftpuser`   
⑥ Select Advanced...   

![winscp_desktop_newsite1](imgs/winscp_desktop_newsite1.png "")

Authenticate:  
① Select Authentication
② Click "..." to select .PPK file
![winscp_desktop_authen1](imgs/winscp_desktop_authen1.png "")

Click "Save":  
![winscp_desktop_newsite2](imgs/winscp_desktop_newsite2.png "")

Click "Login" to authenticate SFTP:  
![winscp_desktop_login](imgs/winscp_desktop_login.png "")

Click "Yes" to authenticate SFTP:  
![winscp_desktop_authen2](imgs/winscp_desktop_authen2.png "")

This is screen when you authenticate successfully,  
you have all permission on folder `datadrive-shared`:  
![winscp_desktop_loginsuccess](imgs/winscp_desktop_loginsuccess.png "")

### Using FileZilla

Create New Site:
① Select New Site.  
② Select General tab.  
③ Select SFTP protocol.  
④ Paste the SFTP Enpoint (`sftpUrl`)  
⑤ Select Port: 22  
⑥ Select Logon type: Key file  
⑦ Input User name: `sftpuser`   
⑧ Select Browse to choose .PPK file...  

![filezilla_desktop_newsite1](imgs/filezilla_desktop_newsite1.png)

If evrything ok, you will access to SFTP Server
---