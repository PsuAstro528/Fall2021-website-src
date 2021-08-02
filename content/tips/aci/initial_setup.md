+++
title = "Initial Setup for Astro 528 on ACI"
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

## TODO: Need to update this page for Fall 2021 

<a id="setup-julia"></a>
### Setup Julia kernel to work with ACI's Jupyter notebook server

- Browse to portal.aci.ics.psu.edu
- Login (if necessary)
- Click _Interactive Apps_ on top menu
- Before using Julia on ACI for the first time
   + Choose _ACI Interactive Desktop_
   + Click _Launch_
   + Wait while your job starts
   + Once the _Launch noVNC in new tab_ button appears, click it
- Open a terminal via second button on bottom toolbar
- Run the following code in the terminal

```shell
module load python/3.6.3-anaconda5.0.1
cd work
mkdir julia_depot
# Setup a Julia package depot in your ACI work directory
cd julia_depot
export JULIA_DEPOT_PATH=$PWD
echo "export JULIA_DEPOT_PATH=$PWD" >> ~/.bashrc
cd ..

# Install Julia in your work directory
mkdir julia_install
cd julia_install/
wget https://julialang-s3.julialang.org/bin/linux/x64/1.0/julia-1.0.2-linux-x86_64.tar.gz
tar -xf julia-1.0.2-linux-x86_64.tar.gz
cd julia-1.0.2

# Setup paths so Julia can be found
# If you've not used ICS-ACI before (or have used it without changing the
# default settings), then the follow lines should work.
export PATH=$PWD/bin:$PATH
export LD_LIBRARY_PATH=$PWD/lib:$LD_LIBRARY_PATH
export LD_LIBRARY_PATH=$PWD/lib/julia:$LD_LIBRARY_PATH
echo "export PATH=$PWD/bin:$PATH" >> ~/.bashrc
echo "export LD_LIBRARY_PATH=$PWD/lib:$LD_LIBRARY_PATH" >> ~/.bashrc
echo "export LD_LIBRARY_PATH=$PWD/lib/julia:$LD_LIBRARY_PATH" >> ~/.bashrc
# But if you have already been using ICS-ACI, then you may have adjusted
# your default paths in a way that prevents the ICS-ACI portal from starting
# properly.  (Or a program may have done it for you.  In that case, I
# suggest commenting out the lines of your .bashrc, .bash_profile,
# .bash_login or .profile that set your PATH variable.
# Then logout of aci-i and log back in, so that you're back to the "default"
# PATH.  Then try following command (not commented out)
# export PATH=${PATH}:/storage/home/ebf11/work/julia_install/julia-1.0.2/bin:/opt/aci/sw/python/3.6.3_anaconda-5.0.1/scripts:/usr/lib64/qt-3.3/bin
# to update your path default to including julia and python.


# Setup IJulia and a few packages that we'll be using lots
julia -e 'using Pkg; Pkg.add(["IJulia","Weave","NBInclude", "Pluto", "PlutoUI"])'
```

- If you do not already have ssh keys setup on ICS-ACI, then create them with:
```shell
# Create ssh-keys (unless you've already done that on ACI)
ssh-keygen -t rsa -b 4096  # follow prompts, default location should be ok
cat ~/.ssh/id_rsa.pub
```

- If this is your first time using git, then enter something for your name and email (you may wish to use your github id rather than your real name, and a non-email address like nobody@nowhere.org).

```shell
git config --global user.email "nobody@nowhere.org"
git config --global user.name "Your Github Id"
```

- Authorize your ssh-keys on GitHub, following [these instructions](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/#platform-linux) but manually copying the key rather than using xclip (i.e., starting from step 2)
- Shutdown the session and close the browser window/tab with the ACI Interactive Desktop
- Go back to the "My Interactive Sessions" tab in the ACI Portal, click "Delete" for this Sessions and confirm.

 

