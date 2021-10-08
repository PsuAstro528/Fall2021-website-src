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
   - Run GPU code on ICDS-ACI
   - Accelerate linear algebra computations with GPU
   - Recognize what problem sizes and likely to result in acceleration with a GPU for linear algebra
- Lab 8, Exercise 2:
   - Perform custom scientific computations using high-level GPU interface, such as
      + [Folds.jl](https://juliafolds.github.io/Folds.jl/dev/) with `CUDAEx()` executor from [FoldsCUDA.jl](https://juliafolds.github.io/FoldsCUDA.jl/dev/) (recommended), or
      + `mapreduce` on [`CuArray`](https://cuda.juliagpu.org/stable/usage/array/) from [CUDA.jl](https://cuda.juliagpu.org/stable/) (recommended)
   - Improve performance by reducing kernel launches via broadcasting and GPU kernel fusion
   - Improve performance by reducing memory transfers via GPU reductions
   - Recognize what types of problems and problem sizes are likely to result in acceleration with a GPU  when using a high-level programming interface
- Lab 8, Exercise 3:
   - Write a GPU kernel, using one of
      + [CUDA.jl](https://cuda.juliagpu.org/stable/tutorials/introduction/#Writing-your-first-GPU-kernel)
      + [FoldsCUDA.jl](https://juliafolds.github.io/FoldsCUDA.jl/dev/)
      + [KernelAbstractions.jl](https://juliagpu.github.io/KernelAbstractions.jl/stable/)
   - Improve performance through reduced memory usage
   - Recognize when a custom kernel is likely improve GPU performance
- Project
   - Parallelize real world code
   - Achieve significant performance benefit via parallelization
{{%/excerpt%}}

## Resources
- [GPU Workshop at JuliaCon 2021](https://github.com/maleadt/juliacon21-gpu_workshop)
