+++
title = "Learning goals"
course_inst = "Penn State"
course_number = "Astro 528"
course_name = "High-Performance Scientific Computing for Astrophysics"
weight = 02103  #wwdpp

chapter= false
hidden = false

creatordisplayname = "Eric Ford"
creatoremail = "ebf11 at psu dot edu"
lastmodifierdisplayname = "Eric Ford"
lastmodifieremail = "ebf11 at psu dot edu"
+++

# Week 2

{{%excerpt%}}
- Priorities for Scientific Computing
- Exercise 1:  Benchmarking
   + Benchmark functions accurately
   + Predict cost of an algorithm based on Big-O analysis
   + Identify real world complications that affect scaling
- Exercise 2:  Numerical Stability of N-body Integration
   + Integrate differential equations
   + Compare the accuracy and numerical stability of results as a function of time step, order and integration algorithm
   + Appreciate importance of numerical stability
- Exercise 3: Assertions, Unit Tests & Continuous Integration Testing
   + Write effective tests for floating point calculations
   + Reduce bugs via _assertions_
   + Identify bugs promptly via _unit testing_
   + Identify bugs promptly via _continuous integration testing_
   + End-to-end Testing to validate code
{{%/excerpt%}}

## Lessons along the way

+ [Just-in-Time (JIT) Compilation](https://en.wikipedia.org/wiki/Just-in-time_compilation)
+ Types of languages
  - Compiled vs Interpretted vs JIT
  - Static/dynamic type-checking
+ Plotting with [Plots.jl](https://github.com/JuliaPlots/Plots.jl)
+ [Keyword/Named function arguements](https://docs.julialang.org/en/v1/manual/functions/index.html#Keyword-Arguments-1)
+ Integration Algorithms
  - [leapfrog](https://en.wikipedia.org/wiki/Leapfrog_integration)
  - [symplectic](https://en.wikipedia.org/wiki/Symplectic_integrator)
<!-- + [view(array, inds...)](https://docs.julialang.org/en/v1/base/arrays/#Views-(SubArrays-and-other-view-types)-1) -->
