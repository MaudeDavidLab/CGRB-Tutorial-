# Getting Set Up

## Get a CGRB Account
1.	If you do not have an CGRB account, then you will need to create one by filling out the form at: http://shell.cgrb.oregonstate.edu/access/
2.	Have a graduate student email Chris Sullivan to make sure the process moves quickly. cc Maude

## Getting a Terminal:
### Windows Users: Download a free Secure Shell (ssh). You can use either Moba or Putty. I recommend Moba. 
#### Option 1: Moba
•	Download MobaXterm: https://mobaxterm.mobatek.net/download-home-edition.html (Use Installer Edition)

•	Once you have a CGRB account and installed MobaXterm, open MobaXterm. Go to Sessions -> New Session, and click on the SSH icon.

•	Enter shell.cgrb.oregonstate.edu as the remote host, and click on the Specify Username (this is your ONID) checkbox to enter your username in the appropriate field. Change port to 732

•	Click on the Bookmark settings tab to save your session with a specific name, e.g. CGRB

•	The CGRB session you just created will connect, and you will be asked to enter your
password at the prompt. **Note: You will not see anything as you type your password. This is a security feature in Linux!!!
•	After a successful logon, press enter at the prompt below: Terminal type? [xterm]
•	Then you get a prompt that looks something like this:

#### Option 2: Putty
•	Download Putty here: http://the.earth.li/~sgtatham/putty/latest/x86/putty.exe
•	Once you have the software, launch PuTTY and you will see the following screen:

•	In the "Host Name (or IP address)" field, type: "shell.cgrb.oregonstate.edu"
•	Change the port to 732
•	Select open
•	You will then be prompted to enter your username and password

### Mac or Linux Users: 
You have a terminal w/ ssh built into the OS. Open the terminal, and at the prompt, type:  
`ssh onidusername@shell.cgrb.oregonstate.edu -p 732`

## Get VPN
If you are connecting off-campus, you must first have a VPN. Follow the tutorial: https://cosine.oregonstate.edu/faqs/vpn

## Map Network Drive
Lastly, you want to map a network drive to the CGRB server. This allows you to directly work off the server as if it were a disk drive on your computer. You can follow these instructions to map a network drive for Windows or MacOS.

#### Windows:

1.	Open "This PC" by clicking the start menu, indicated by this iconStart menu, and then searching "This PC"

2.	On the top bar, select "Computer"

3.	Select "Map network drive"

4.	Select the "Z" drive letter. (If Z is already taken, another drive letter may be used.) In the "Folder" text field, enter the path to the folder you wish to access.
Folder pre-path should be: \\files.cgrb.oregonstate.edu\NFS_PHARM\David_lab
\YOUR_FOLDER

5.	You will then be prompted to enter your security credentials

a.	Username: ONID\YOURONID

b.	Password: Enter your email password


#### MacOS:


1.	From the desktop, go to the top bar and select "Go", then select "Connect to Server..."


2.	In the window that opens, select the "Server Address:" field and type "smb:" followed by the path you wish to access. This is: smb://files.cgrb.oregonstate.edu/NFS_PHARM/David_lab/YOUR_FOLDER


3.	Click on the "+" button to the right of the address bar to add the path to your favorites so that you won't have to retype it next time you connect via this method.


4.	You will then be prompted to enter your security credentials


a.	Username: ONID\YOURONID


b.	Password: Enter your email password


## Symbolic link to mapped drive
https://www.infopackets.com/news/10088/how-fix-cant-access-mapped-network-drive-administrative-command-prompt
