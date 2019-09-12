### Installing Google Drive Ocamlfuse on Ubuntu 18.04

To install the Google Drive Ocamlfuse run the following commands in that order

```
$ sudo add-apt-repository ppa:alessandro-strada/ppa
$ sudo apt-get update
$ sudo apt-get install google-drive-ocamlfuse
```

Once successfully installed, authorize google-drive-ocamlfuse client with your desired Google account using the following command.

```
# google-drive-ocamlfuse
```

This is going to pop open a page on your browser where Google will request you to choose a Gmail  account to continue with the setup

This is going to pop open a page on your browser where Google will request you to choose a Gmail  account to continue with the setup

![img](https://linoxide.com/wp-content/uploads/2018/12/ocamlfuse-choose-an-account.png)

Next, Gdfuse will request access to your account.

![img](https://linoxide.com/wp-content/uploads/2018/12/ocamlfuse-wants-to-access-your-account.png)

Click on the 'Allow' button to allow google-drive-ocamlfuse to access your Google Drive.

You'll then be prompted for your password

![img](https://linoxide.com/wp-content/uploads/2018/12/ocamlfuse-password-prompt.png)

You will then be asked to choose the account to use

![img](https://linoxide.com/wp-content/uploads/2018/12/ocamlfuse-select-account-to-use.png)

Finally, create a mount point in your home directory and mount the directory

```
$ mkdir ~/gdrive
$ google-drive-ocamlfuse ~/gdrive
```

You should be set!

