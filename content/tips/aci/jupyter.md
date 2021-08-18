+++
title = "Jupyter Notebooks on ACI"
course_inst = "Penn State"
course_number = "Astro 528"
course_name = "High-Performance Scientific Computing for Astrophysics"
weight = 0824

chapter= false
hidden = false

creatordisplayname = "Eric Ford"
creatoremail = "ebf11 at psu dot edu"
lastmodifierdisplayname = "Eric Ford"
lastmodifieremail = "ebf11 at psu dot edu"
+++

### Start a JupyterLab server configured to offer the Julia kernel on ACI
Each time in the future you want to start a Jupyter notebook session on ICDS-ACI.

- Make sure you have an account on ACI and have completed the [initial setup](/tips/aci/initial_setup)
- Browse to portal.aci.ics.psu.edu
- Login (if necessary)
- Click _Interactive Apps_ on top menu
- Choose _BYOE Jupyter Server__
    + Select:
        - Jupyter Interface: JupyterLab
        - Environment setup: `source /gpfs/group/RISE/sw7/conda_envs/julia/env/setup`
        - Allocation: ebf11_d_g_gc_default
        - Number of hours: 2 hours  (can choose longer if you plan to continue after class or outside of class)
        - Number of cores: 2 (can choose more outside of class time once start parallel labs and project)
        - Node type: ACI-b GPU (either No GPU or 1 GPU once start GPU lab or for project)
        - Memory per core: 4 GB (can choose more outside of class time once start project)
    + Click _Launch_
    + Wait while your job starts
- Once the _Connect to JupyterLab Server_ button appears, click it
    + The top row of tiles (labeled "Notebook") should include a tile labeled "Julia 1.6.0".  Click it.  
    + A new browser tab should open where you can work with a Jupyter notebook using a Julia kernel interactively.
    + Do your work, remembering to save your notebook after key edits and before you quit.
- See [Starting & Submittiing Assignments](/tips/submitting) for more information on accessing and submitting assignments.
- When you're done, close notebook tabs and click logout in upper right (of the Jupyter server session).
- Go back to the "My Interactive Sessions" tab in the ACI Portal, click "Delete" for this Sessions and confirm.

