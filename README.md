# Bashes
create_n_run is a bash shell script to automatically generate input and job files and submit them to queue.
celllist runs the unit cell calculation, generate a list of mof ids and cell sizes
screening does the actual screening and submits the jobs
result analyzes the result in the folders


03/29/19
the Finer_JOBCHECK code counts how many jobs are there either Running(R) or Waiting(Q) or Terminated(C). Since northwestern's quest machine only allows 500 total jobs simultaneously, the number of jobs you can submit is 500 - number of jobs with R/Q/C. Keep doing "./ Finer_JOBCHECK" will give you a CONTINUOUS flow of jobs. If your jobs take a long time to run, simply change the time of sleeping between each job submission to hide the latency.
To run this code, you need to generate a mof list beforehand.

08/31/21
added check_time code that checks how old a slurm file is, if it is not finished. 
