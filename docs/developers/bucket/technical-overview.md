# Managing Files

## Moving / Copying a File to a New Location on Bucket

There are two commands for moving and copying: `mv` and `cp`.

- Copy a file from one directory to another: `cp [path]/file-name [new-location]`
- Move a file from one directory to another: `mv [path]/file-name [new-location]`

Move a file from one directory to another:

1. Connect to VPN.
1. In terminal, log into the server.
1. CD into root: `cd /`
1. Check your directory to verify you’re in PLIE09 root: `pwd`
1. Look-see what is in the folder: `ls -la`
1. Go to data/www: `cd data/www`
1. Look-see what is in the folder: `ls -la`
1. Move your file out of the old bucket and into assets folder: `mv easy-reader-dot-blue.jpg ../../assets/images/easy-reader-dot-blue.jpg`

## Change Permissions on a File or Directory

- Change permissions for a single file or directory: `sudo chown apache:apache [name of file or folder]`
- Change permissions for all the files in a directory: `sudo -R chown apache:apache [name of folder]`
