## 0. Ask Chris Sullivan to add your username to the list of people who can ssh into mus for xtunneling. He needs to give you permissions in order for this to work.

These are instructions for windows users. 
## 1. Enable tunneling on your location machine. 
#### - Download Xming from https://sourceforge.net/projects/xming/ 
#### - Run the executable to install it
#### - Once it installs, launch it. You won't see a window pop up. Make sure it's running by checking the tray of passive programs at the bottom right of your tool bar: ![image](https://user-images.githubusercontent.com/5238386/121963172-9d7f2300-cd1e-11eb-8cde-d32c265175a9.png)

## 2. Enable xtunneling on your ssh client. I use Putty
#### - Go into Connection, SSH, X11 and check the box for "Enable X11 forwarding"
![image](https://user-images.githubusercontent.com/5238386/121963367-e1722800-cd1e-11eb-813a-961be5c22330.png)

#### - click open to ssh into vaughan, the log-in node

## 3. Check out some processors that will be used for tunneling
#### - `qrsh -q mus -pe thread #`
![image](https://user-images.githubusercontent.com/5238386/121963542-1bdbc500-cd1f-11eb-8b4a-d6a657da1aea.png)

## - leave that window open!!

## 4. SSH into the processors you just checked out
#### - Using Putty, open a new session on the login node. Don't touch the session where you just checked out the processors. Leave that up.
#### - In your new session, use `ssh -X mus#` (whichever mus machine you checked out. Go look, was it 1 or 2?) to logon to the mus processors
#### - Use the command 'xeyes' to test that the connection works. You should see a pair of googly eyes that track your mouse show up on your screen!
![image](https://user-images.githubusercontent.com/5238386/121964179-fa2f0d80-cd1f-11eb-9f51-3f5c37eae7d5.png)


## It's VERY important that you check out the processors before using them for xtunneling. Otherwise, jobs will still be submitted to them from the regular job queue, and the machines will crash, causing potentially days of downtime!
