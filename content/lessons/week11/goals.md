+++
title = "Learning goals"
course_inst = "Penn State"
course_number = "Astro 528"
course_name = "High-Performance Scientific Computing for Astrophysics"
weight = 11103  #wwdpp

chapter= false
hidden = false

creatordisplayname = "Eric Ford"
creatoremail = "ebf11 at psu dot edu"
lastmodifierdisplayname = "Eric Ford"
lastmodifieremail = "ebf11 at psu dot edu"
+++

# Week 11

{{%excerpt%}}
- Lab 8, Exercise 1
   - Run GPU code on ICDS-ACI/Roar
   - Accelerate linear algebra computations with GPU
   - Recognize what problem sizes and likely to result in acceleration with a GPU for linear algebra
- Lab 8, Exercise 2:
   - Write a GPU kernel, using [KernelAbstractions.jl](https://juliagpu.github.io/KernelAbstractions.jl/stable/)
   - Improve performance by reducing kernel launches via broadcasting and GPU kernel fusion
   - Improve performance by reducing memory transfers via GPU reductions
   - Perform custom scientific computations using high-level GPU interface, such as
      + `map` or `mapreduce` on [`CuArray`](https://cuda.juliagpu.org/stable/usage/array/) from [CUDA.jl](https://cuda.juliagpu.org/stable/) (recommended), or
      - Recognize what types of problems and problem sizes are likely to result in acceleration with a GPU  when using a high-level programming interface or custom GPU kernel
      + [Folds.jl](https://juliafolds.github.io/Folds.jl/dev/) with `CUDAEx()` executor from [FoldsCUDA.jl](https://juliafolds.github.io/FoldsCUDA.jl/dev/)
   - Improve performance through reduced memory usage
- Project
   - Parallelize real world code
   - Achieve significant performance benefit via parallelization
{{%/excerpt%}}

## Resources
- [GPU Workshop at JuliaCon 2021](https://github.com/maleadt/juliacon21-gpu_workshop)
