+++
title = "Lab 1: Tools & Fundamentals"
course_inst = "Penn State"
course_number = "Astro 528"
course_name = "High-Performance Scientific Computing for Astrophysics"
weight = 0301  #3nn

chapter= false
hidden = false

creatordisplayname = "Eric Ford"
creatoremail = "ebf11 at psu dot edu"
lastmodifierdisplayname = "Eric Ford"
lastmodifieremail = "ebf11 at psu dot edu"
+++


{{%excerpt%}}
[Lab 1: **Tools & Fundamentals: Floating Point Arithmetic, Functions, Tests**](https://github.com/PsuAstro528/lab1-start)
(Due Sept 2)

- [Exercise 1](https://psuastro528.github.io/lab1-start/ex1.html): Get started using core development tools
    + [ICDS-ACI portal](http://portal.aci.ics.psu.edu/)
    + [git](https://try.github.io/)
    + [GitHub.com](https://github.com)
    + [Julia](https://julialang.org/)
    + [Pluto Notebooks](https://github.com/fonsp/Pluto.jl)
- [Exercise 2](https://psuastro528.github.io/lab1-start/ex2.html): Floating Point Arithmetic, Functions, Tests
- Exercise 3: Personal Goals (save at least 15 minutes for this one)
{{%/excerpt%}}

If you're waiting on getting your account on ICDS-ACI, then I'd suggest that you start with exercise 3, since thinking about your goals does not require any accounts or special software.

If you're still waiting on getting your account on ICDS-ACI, then you could using a local installation of Julia.
If that gives you trouble, then you could use [JuliaHub](https://juliahub.com/) or [Binder](https://mybinder.org) to start tinkering on the assignments.    For running Pluto notebooks on Binder, you can use [Pluto.jl on Binder](https://pluto-on-binder.glitch.me/).  From the html versions linked above, click "Edit or run this notebook" in the upper right and then click the binder button.  Be patient, as it'll take a while to build a virtual machine for you to use.

Note that you will not be able to save your work directly to a github repository when using Binder.  Instead, you could click the triangle and circle icon in the upper right and choose to download a "Notebook file" exiting your session.  Then you could copy it into your github repository.  While this is workable for the first few labs, you'll need to get ACI working for later assignments where performance is actually important part of the assignment.

## Additional Resources
- [Getting Started with Julia on ACI](/tips/aci)
- [Starting & Submitting Assignments](/tips/submitting)
- [Julia Resources](/resources/julia)


{{< children depth="1" >}}
