+++
title = "Jupyter Notebooks on ACI"
course_inst = "Penn State"
course_number = "Astro 528"
course_name = "High-Performance Scientific Computing for Astrophysics"
weight = 0820

chapter= false
hidden = false

creatordisplayname = "Eric Ford"
creatoremail = "ebf11 at psu dot edu"
lastmodifierdisplayname = "Eric Ford"
lastmodifieremail = "ebf11 at psu dot edu"
+++

## TODO:  Need to update this page for Fall 2021 

<a id="start-jupyter"></a>
### Start a Jupyter notebook session on ACI
Each time in the future you want to start a Jupyter notebook session on ICS-ACI

- Make sure you have an account on ACI and have completed the [initial setup](/tips/aci/initial_setup)
- Browse to portal.aci.ics.psu.edu
- Login (if necessary)
- Click _Interactive Apps_ on top menu
- Choose _Jupyter Notebook_
    + Select:
        - Anaconda version: 5.0.1-3.6.3
        - Allocation: Open
        - Number of hours: 2 hours
        - Node type: ACI-i
    + Click _Launch_
    + Wait while your job starts
- Once the _Connect to Jupyter Notebook Server_ button appears, click it
    + Near the upper right, there's a _New_ button, from which you can create a new blank notebook using Julia 1.0.2 or access a terminal or text editor.
    + If you'd like to create a blank notebook, then choose _New.Julia 1.0.2_
    + A new browser tab should open where you can work with a notebook interactively.
    + Do your work, remembering to save your notebook after key edits and before you quit.
- See [../submitting](Starting & Submitting Assignments) for more information on accessing and submitting assignments.
- When you're done, close notebook tabs and click logout in upper right (of the Jupyter server session).
- Go back to the "My Interactive Sessions" tab in the ACI Portal, click "Delete" for this Sessions and confirm.

