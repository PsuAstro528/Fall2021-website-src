+++
title = "ACI Remote Desktop"
weight = 828
type="page"
include_toc = true

creatordisplayname = "Eric Ford"
creatoremail = "ebf11@psu.edu"
lastmodifierdisplayname = "Eric Ford"
lastmodifieremail = "ebf11@psu.edu"
+++

## Starting a Remote Interactive Desktop session on ACI

To start a remote Interactive Desktop session:
- Log into the [ICDS-ACI Portal at https://portal.aci.ics.psu.edu/](https://portal.aci.ics.psu.edu/).
- Choose *Interactive Apps*, *RHEL7 Interactive Desktop*.
- Choose MATE (Gnome 2) for Dektop Environment.
- Select "ebf11_d_g_gc_default" for allocation and "ACI-b GPU Core" for node type.  (Alternatively, one might choose open for allocation and "ACI-i" for node type.) 
- Choose number of hours that you will be using the Interactive Desktop for this session.  
- Click "Launch"
- Wait a little while, as your the system will submit a job to the scheduler.
- Once you have a button to start your session, click it.
- A new browser tab will open with a virtual desktop.

## Starting Julia from the terminal

- Open a terminal window by clicking Applications, System Tools, Terminal.
- If you ran the `/gpfs/group/RISE/classroom/astro_528/scripts/class_setup setup` at the beginning of the smester, then julia 1.6.0 will already be in your path.  If not, then from the terminal, setup your environment variables to know about Julia 1.6 by running: 
```shell
module use /gpfs/group/RISE/sw7/modules
module load julia/1.6.0
```
- Start Julia by running
```shell
julia
```

## Starting a Pluto session

- If you'd like to launch a Pluto notebook server, you can install [Pluto](https://github.com/fonsp/Pluto.jl) from within Julia with
```julia
using Pkg
Pkg.add("Pluto")
```
and then start it by running
```julia
using Pluto
Pluto.run()
```

## Starting a Jupyter notebook session

- If you'd like to launch a Jupyter notebook server, you can install [IJulia](https://github.com/JuliaLang/IJulia.jl) from within Julia with 
```julia
using Pkg
Pkg.add("IJulia")
```
and then start the Jupyter notebook by running
```julia
using IJulia
notebook()
```

