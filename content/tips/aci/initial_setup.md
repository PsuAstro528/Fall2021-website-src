+++
title = "Initial Setup on Roar"
course_inst = "Penn State"
course_number = "Astro 528"
course_name = "High-Performance Scientific Computing for Astrophysics"
weight = 0814

chapter= false
hidden = false

creatordisplayname = "Eric Ford"
creatoremail = "ebf11 at psu dot edu"
lastmodifierdisplayname = "Eric Ford"
lastmodifieremail = "ebf11 at psu dot edu"
+++

## Initial Setup for Roar / ICDS-ACI


1.  [Request an account on "Roar"](../create_acount), the supercomputing facility run by Penn State's Institute for Computational and Data Science (ICDS) Advanced CyberInfrastructure (ACI) group.  

2. Once your account is active, go to the [ACI portal](https://portal.aci.ics.psu.edu), go to Clusters._ACI Shell Access.

3. Run '/gpfs/group/RISE/classroom/astro_528/scripts/updateKeys.sh’ to [setup your ssh keys on ACI](../sshkeys).  You can accept most of the default prompts, but I recommend that you do NOT enter a password for your ssh key (we'll discuss why in a few weeks).  If you do use a password, then you’ll have extra work to do before Lab 7. 

4.  Authorize your ssh-keys on GitHub, as described in [SSH keys on ACI](../sshkeys).

5. If this is your first time on ACI (or first time using git on ACI), then [configure git](../git).
 
6. Make a few updates to your ACI environment.  To make this easy, Justin has provided a script that you can easily run from ACI, `/gpfs/group/RISE/classroom/astro_528/scripts/class_setup setup`. If you’re curious, this will update your .bashrc startup script so that it automatically loads a module (so software for the course is in your path; `module use /gpfs/group/RISE/sw7/modules`), and move your .julia and .conda directories from the home filesystem to the work filesystem (since those can get rather large).  If you already have customized your Roar envivironment for your research, then you may want to look at the script and make changes incrementally, so you don’t accidentally break something.  If something does break, you can run `/gpfs/group/RISE/classroom/astro_528/scripts/class_setup restore` to undo the setup changes above.  

7. Exit from the console and you should be good to go! 

