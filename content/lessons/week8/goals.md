+++
title = "Learning goals"
course_inst = "Penn State"
course_number = "Astro 528"
course_name = "High-Performance Scientific Computing for Astrophysics"
weight = 08103  #wwdpp

chapter= false
hidden = false

creatordisplayname = "Eric Ford"
creatoremail = "ebf11 at psu dot edu"
lastmodifierdisplayname = "Eric Ford"
lastmodifieremail = "ebf11 at psu dot edu"
+++

# Week 8

{{%excerpt%}}
- Lab 6:  Shared Memory Computing Patterns
   - Choose an appropriate number of worker processors for your compute node & problem
   - Parallelize code for shared memory model, using patterns such as:
      + [FLoops.jl](https://juliafolds.github.io/FLoops.jl/dev/) and `ThreadedEx` (recommended)
      + [Threads.@threads](https://docs.julialang.org/en/v1/manual/multi-threading/#The-@threads-Macro) and/or [ThreadsX.jl](https://tkf.github.io/ThreadsX.jl/dev/) for for loops (recommended)
      + [Folds.jl](https://github.com/JuliaFolds/Folds.jl) (alternative)
      + [SharedArray](https://docs.julialang.org/en/v1/stdlib/SharedArrays/)s (alternative)
- Readings / Discussions
   - Evaluating the suitability of a problem for different parallel architectures
{{%/excerpt%}}

## Lessons along the way
- Reinforce programming patterns demonstrated in [Lab 5](/labs/lab5)
   - Organize code into files and a [module](https://docs.julialang.org/en/v1/manual/modules/index.html)
   - Using [function-like objects](https://docs.julialang.org/en/v1/manual/methods/#Function-like-objects-1)
   - Using [broadcasting](https://docs.julialang.org/en/v1/base/arrays/#Broadcast-and-vectorization-1)
   - Using [abstract types](https://docs.julialang.org/en/v1/manual/types/#Abstract-Types-1)
   - Using [parametric types](https://docs.julialang.org/en/v1/manual/types/#Parametric-Types-1)
