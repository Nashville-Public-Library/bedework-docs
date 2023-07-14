# Add or Update Content on a Bucket Site

## Set Up Your Workstation

### For PC

1. Install git on the PC.
1. Choose a command line program:
      1. Default: Use the default command line program that comes with a PC.
      1. Git Bash: Download “git bash” and install it for use instead.

### For Mac

1. Open terminal. Git is already there.

## Update Site Content

### Edit Existing Content

If you are off-site, you will need to log in to VPN to interact with Bucket.

1. Open terminal (Mac) or command line (PC).
1. Log in to Bucket. Login should be in a password manager.
1. Navigate to the site directory:  
`cd /data/www/[site-name]`
1. Pull code:  
`git pull`
1. Navigate to your site files on your local:  
`cd [path-to-your-local-files]`
1. Open the page you need to update in a text editor, like Atom or Sublime Text.
1. Make your changes and save your work.
1. In terminal / command line, commit your work then push your work to Github:
      1. `git status`
      1. `git add [file]`
      1. `git commit -m [message]`
      1. `git push origin master`
1. In terminal / command line, pull your changes from Github to Bucket:  
`git pull origin master`
1. Navigate to the site directory:  
`cd /data/www/[site-name]`
1. Pull code to Bucket:
      1. `sudo git pull origin master`
      1. Type your sudo password for Bucket.
      1. Type your github.com username.
      1. Type your github password.
1. Visit [site-name].library.nashville.org to verify that the changes are present.

### Add New Content

If you are off-site, you will need to log in to VPN to interact with Bucket.

1. Open terminal (Mac) or command line (PC).
1. Log in to Bucket. Login should be in a password manager.
1. Navigate to the site directory:  
`cd /data/www/[site-name]`
1. Pull code:  
`git pull`
1. Navigate to your site files on your local:  
`cd [path-to-your-local-files]`
1. Create a new page in a text editor, like Atom or Sublime Text.
1. Make your changes and use “save as” to save your work to the site directory on your local:  
`cd [path-to-your-local-files]`
1. In terminal / command line, commit your work then push your work to Github:
      1. `git status`
      1. `git add [file]`
      1. `git commit -m [message]`
      1. `git push origin master`
      1. In terminal / command line, pull your changes from Github to Bucket:  
      `git pull origin master`
      1. Navigate to the site directory:  
      `cd /data/www/[site-name]`
      1. Pull code to Bucket:
         1. `sudo git pull origin master`
         1. Type your sudo password for Bucket.
         1. Type your github.com username.
         1. Type your github password.
   1. Visit [site-name].library.nashville.org to verify that the changes are present.
