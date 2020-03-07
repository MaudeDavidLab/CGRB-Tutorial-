When using the server, you cannot do your work on the login node (waterman). You must do one of two things: 
1. you can login to a compute node in interactive mode and do your work live. This is best if you have a small job, or if you want to iterate on a script.
2. you can submit your job to be run on a compute node. This is best if you have a large job.

### Interactive mode
1. use SGE_Avail to see a list of the compute nodes you have access to. You may see something like the following:
![SGE_Avail](/screen_shots/SGE_Avail.png)
