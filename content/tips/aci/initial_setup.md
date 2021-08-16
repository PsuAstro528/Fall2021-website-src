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

5. If this is your first time on ACI (or first time using git on ACI), then enter something for your name and email (you may wish to use your github id rather than your real name, and a non-email address like nobody@nowhere.org).

```shell
git config --global user.email "nobody@nowhere.org"
git config --global user.name "Your Github Id"
```
6. Exit from the console and you should be good to go! 

