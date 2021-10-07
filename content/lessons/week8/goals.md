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
   - Parallelize code using shared memory model & multiple threads, using tools such as:
      + [ThreadsX.map](https://tkf.github.io/ThreadsX.jl/dev/) and ThreadsX.mapreduce
      + [Threads.@threads](https://docs.julialang.org/en/v1/manual/multi-threading/#The-@threads-Macro)
      + [ThreadsX.foreach](https://tkf.github.io/ThreadsX.jl/dev/)
      + [FLoops.jl](https://juliafolds.github.io/FLoops.jl/dev/) and `ThreadedEx` (recommended)
      + [Threads](https://docs.julialang.org/en/v1/manual/multi-threading/)
      + [Folds.jl](https://github.com/JuliaFolds/Folds.jl) (alternative)

   - Parallelize code using shared memory model & multiple processes, using tools such as:
      + [pmap](https://docs.julialang.org/en/v1/stdlib/Distributed/#Distributed.pmap)
      + [SharedArray](https://docs.julialang.org/en/v1/stdlib/SharedArrays/)s
      + [DistributedArrays.jl](https://juliaparallel.github.io/DistributedArrays.jl/stable/) w/ using map and mapreduce
      + [@distributed for loop](https://docs.julialang.org/en/v1/stdlib/Distributed/#Distributed.@distributed)    
      + [FLoops.jl](https://juliafolds.github.io/FLoops.jl/dev/) and `DistributedEx` (recommended)
      + [Folds.jl](https://github.com/JuliaFolds/Folds.jl) (alternative)
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
