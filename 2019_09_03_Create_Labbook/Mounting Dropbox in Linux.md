# Mounting Dropbox in Linux

#### Installing dbxfs

The dbxfs officially supports Linux and Mac OS. However, it should work on any POSIX system that provides a **FUSE-compatible library** or has the ability to mount **SMB** shares. Since it is written for Python 3.5, it can installed using **pip3** package manager. Refer the following guide if you haven’t installed PIP yet.

- [**How To Manage Python Packages Using Pip**](https://www.ostechnix.com/manage-python-packages-using-pip/)

And, install FUSE library as well.

On Debian-based systems, run the following command to install FUSE:

```
$ sudo apt install libfuse2
```

On Fedora:

```
$ sudo dnf install fuse
```

Once you installed all required dependencies, run the following command to install dbxfs utility:

```
$ pip3 install dbxfs
```

#### Mount Dropbox folder locally

Create a mount point to mount your dropbox folder in your local file system.

```
$ mkdir ~/mydropbox
```

Then, mount the dropbox folder locally using dbxfs utility as shown below:

```
$ dbxfs ~/mydropbox
```

You will be asked to generate an access token:

[![Generate access token 1](https://www.ostechnix.com/wp-content/uploads/2018/10/Generate-access-token-1.png)](https://www.ostechnix.com/wp-content/uploads/2018/10/Generate-access-token-1.png)

Generate access token

To generate an access token, just navigate to the URL given in the above output from your web browser and click **Allow** to authenticate Dropbox access. You need to log in to your dropbox account to complete authorization process.

[![Authorize dropbox](https://www.ostechnix.com/wp-content/uploads/2018/10/Authorize-dropbox.png)](https://www.ostechnix.com/wp-content/uploads/2018/10/Authorize-dropbox.png)

Authorize dropbox

A new authorization code will be generated in the next screen. Copy the code and head back to your Terminal and paste it into cli-dbxfs prompt to finish the process.

You will be then asked to save the credentials for future access. Type **Y** or **N** whether you want to save or decline. And then, you need to enter a passphrase twice for the new access token.

Finally, click **Y** to accept **“/home/username/mydropbox”** as the default mount point. If you want to set different path, type **N** and enter the location of your choice.

[![Generate access token 2](https://www.ostechnix.com/wp-content/uploads/2018/10/Generate-access-token-2.png)](https://www.ostechnix.com/wp-content/uploads/2018/10/Generate-access-token-2.png)

All done! From now on, you can see your Dropbox folder is locally mounted in your filesystem.