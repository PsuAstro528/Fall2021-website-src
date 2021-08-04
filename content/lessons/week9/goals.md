+++
title = "Learning goals"
course_inst = "Penn State"
course_number = "Astro 528"
course_name = "High-Performance Scientific Computing for Astrophysics"
weight = 09103  #wwdpp

chapter= false
hidden = false

creatordisplayname = "Eric Ford"
creatoremail = "ebf11 at psu dot edu"
lastmodifierdisplayname = "Eric Ford"
lastmodifieremail = "ebf11 at psu dot edu"
+++

# Week 9

{{%excerpt%}}
- Lab 7, Exercise 1:  Run batch jobs on ICDS-ACI/Roar:
   - Submit a batch job via PBS
   - Read and write data from batch job
   - Run multiple jobs using a job array
- Lab 7, Exercise 2:  Parallelize code for Distributed memory model, using patterns such as:
   + Load code and packages on worker nodes
   + Parallelize code using [pmap](https://docs.julialang.org/en/v1/stdlib/Distributed/#Distributed.pmap) (recommended)
   + Parallelize code using [FLoops.jl](https://juliafolds.github.io/FLoops.jl/dev/) and `ThreadedEx` (recommended)
   + Parallelize code using [Dagger.jl](https://juliaparallel.github.io/Dagger.jl/dev/) (alternative)
   + [@distributed for loop](https://docs.julialang.org/en/v1/stdlib/Distributed/#Distributed.@distributed) (alternative)
   + using map and mapreduce on [DistributedArrays.jl](https://juliaparallel.github.io/DistributedArrays.jl/stable/)  (alternative)
   + Explain differences in performance when using multiple processor cores on same node versus using multiple processor cores on different nodes
- Project
   - Run project code as batch job on the ICDS-ACI cluster
- Readings / Discussions
   - Evaluating the suitability of a problem for different parallel architectures
{{%/excerpt%}}

## Lessons along the way
