When using the server, you cannot do your work on the login node (waterman). You must do one of two things: 
1. you can login to a compute node in interactive mode and do your work live. This is best if you have a small job, or if you want to iterate on a script.
2. you can submit your job to be run on a compute node. This is best if you have a large job.

### Interactive mode
1. use SGE_Avail to see a list of the compute nodes you have access to. You may see something like the following:
![SGE_Avail](/screen_shots/SGE_Avail.png)
2. Pick the machine you want to use. Use the following command to login:
`qrsh -q machine_name`
3. You can now do your work! Navigate to your folder in the David_Lab using:
`cd /nfs3/PHARM/David_Lab/your_name`
You can also set up your environment to automatically log you in to this folder! See setup.md for instructions

### Submitting a job
1. The basic syntax of submitting a job:
`SGE_Batch -c "the_command_you_want_to_run" -r "folder_where_your_logs_will_go"`
For more details on options for running a batch job, see http://shell.cgrb.oregonstate.edu/files/cgrb_infrastructure.pdf
2. Once you have submitted your job, you can check to see if it's running using:
 `qstat`
3. If you want to cancel your job for any reason, use `qstat` to get the job-it (ex: 2863594) and then use 
`qdel the_job_id` 
to stop it
