When using software on the remote server, you have three options. 
1. Use the software that is provided by the cgrb. This is the easiest option if the versioning and packages available suit your needs.
2. Copy the cgrb provided software to your local folder, and make whatever changes (i.e. install your own packages). Good if you just need to make a few tweaks.
3. Install your own versions of software from the web

### Using CGRB provided software.
A number of programs are already installed. If you need to use basic R or python, you can login to the server, qrsh into a compute node of your choice, and then call R or python.
You will see a message displaying what verions of the software you are running, and you're good to go


### Copying the software to a local folder
1. navigate to the folder where the cgrb keeps all its software. `cd /local/cluster/`
2. copy the folder with the software you want into your own software folder (which you should make if you haven't already). As an example,
I'll copy R-3.6.1
`cp R-3.6.1/ /nfs3/PHARM/David_Lab/christine/software`
3. cd R-3.6.1/bin
4. R
5. install.packages("your_package_name"). Often, you will get error messages that say you do not have some of the other packages that your package depends on. For example, ERROR: dependencies ‘isoband’, ‘scales’, ‘tibble’ are not available for package ‘ggplot2’
You'll have to install all of these dependencies before you can install your package.

*To Come:
aliases
bashrc for R version

### Installing your own versions

### Creating an allias 
1. Open up your basrc profile  
`vi ~.bashrc`
2. Go to the end of the file and type:
`alias home= 'cd ~/../../../../nfs3/PHARM/David_Lab/YOURFILE/'  
Then exit: `:wq`
3. Install .bashrc profile with one of two ways:
  * Log out and log back in 
  * Run: `source ~/.bashrc`
