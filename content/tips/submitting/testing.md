+++
title = "Testing your labs"
course_inst = "Penn State"
course_number = "Astro 528"
course_name = "High-Performance Scientific Computing for Astrophysics"
weight = 0854

chapter= false
hidden = false

creatordisplayname = "Eric Ford"
creatoremail = "ebf11 at psu dot edu"
lastmodifierdisplayname = "Eric Ford"
lastmodifieremail = "ebf11 at psu dot edu"
+++

<a id="run-tests"></a>
### Test your code

- Make sure you've saved all your changes (Ctrl+S)
- Make sure you've [committed your changes to your local repository](../commit).
- Check that your code passes any tests embedded in each notebook as you go.  
- To test a single exercise, you can use a terminal window, change into your repo directory, and run either:
```julia
julia --project test test/test1.jl
```
- To test al the exercises, you can run
```julia
julia --project test test/runtests.jl
```

- Once you've pushed your changes, it's also good to double check that your lab passes the same test via the continuous integration testing provided by GitHub actions.

<!-- in a separate test notebook like test_myself.ipynb:

```julia
using NBInclude
@nbinclude("exercise1.ipynb")
include("test/test1.jl")
```
- If using a Jupyer notebook, if you make changes and retest, then restart the kernel for the test notebook to be sure there aren't unintended carryover effects.
- Once you think you're done, you are encouraged to test your full repository even more similarly to how it will be tested by the continuous integration testing by opening a terminal window and running `julia test/runtests.jl`
-->
