You may run into the situation where you want to develop on your local machine using either python through jupyter notebooks or R through Rstudio.

### Install Python
The easiest way is to install Anaconda, which is a program that will install python along with a bunch of the most useful python packages.
To install, go to https://www.anaconda.com/distribution/, and download and install the appropriate version for your computer.
(at the bottom of the page, install python 3)

For Mac: just answer yes at every steps

### Give Python access to your mapped drive
#### Windows
1. Follow this tutorial. It will require restarting your computer. https://www.infopackets.com/news/10088/how-fix-cant-access-mapped-network-drive-administrative-command-prompt
2. Open command prompt as adminstrator (open start menu, type command prompt, right click, select 'run as administrator)
3. Make sure you are in your C drive. Type: `mklink /d name_of_your_symbolic_link Z:` assuming you have mapped to your Z drive

### MAC Users:
0. VPN into OSU if you're not on campus + map your files fomr the CGRB (see Map Network Drive in the set-up tutorial)
1. Open your terminal 
2. Create a symbolic link to your mapped files </br>
`ln -s /Volumes/David_lab/YOURFOLDER CGRB_David_lab` </br>
note: you could map the entire David is you wanted 

### Using Python through Jupyter Notebook
### PC USERS
Note: we are going to connect to our mapped file on the CGRB
*You will be using basic terminal commands. If you are not familiar with terminal, go to *SONICA'S PDF* for more instructions.*
1. Go to the start menu, and open Anaconda Prompt. A terminal will open up.
2. Navigate to the folder for you project using cd. If you don't have a project folder yet, make one using mkdir
3. Open jupyter notebook using:
`jupyter notebook`
4. You should be able to see Z_Drive from the steps in "Give Python access to your mapped drive" above.
4. To learn to use jupyter notebook interface, check out this tutorial: https://www.dataquest.io/blog/jupyter-notebook-tutorial/.
Fly down to the heading "What is an ipynb File?" as we've already gone through the installation process.

### Mac USERS
1. Open the terminal
2. Now launch your jupyter notebook in your terminal
`jupyter notebook`
3. You should see in your list of files the CGRB_David_lab which points to your CGRB folder

### Install R
#### follow the protocol here
####FOR MAC
https://courses.edx.org/courses/UTAustinX/UT.7.01x/3T2014/56c5437b88fa43cf828bff5371c6a924/
You need to instal both R and Rstudio 
### Use R with your mapped files: only needed if you have NOT already set this up for jupiter notebook above
You need to create a symbolic link , as explained above, to be able to see loaccly all t=your files that are on the CGRB. 
0. VPN into OSU if you're not on campus + map your files fomr the CGRB (see Map Network Drive in the set-up tutorial)
1. Open your terminal
2. Create a symbolic link to your mapped files </br>
`ln -s /Volumes/David_lab/YOURFOLDER CGRB_David_lab` </br>
note: you could map the entire David is you wanted 
3. Now launch your Rstudio by cliking on it
4. You should see in your list of files the CGRB_David_lab which points to your CGRB folder
