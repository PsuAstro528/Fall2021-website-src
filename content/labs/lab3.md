+++
title = "Lab 3: Memory Hierarchy"
course_inst = "Penn State"
course_number = "Astro 528"
course_name = "High-Performance Scientific Computing for Astrophysics"
weight = 0303  #03nn

chapter= false

creatordisplayname = "Eric Ford"
creatoremail = "ebf11 at psu dot edu"
lastmodifierdisplayname = "Eric Ford"
lastmodifieremail = "ebf11 at psu dot edu"
+++


{{%excerpt%}}
[Lab 3: **Memory Access, Disk I/O, DataFrames**](https://github.com/PsuAstro528/lab3-start)  (due Sept 16)
- [Exercise 1](https://psuastro528.github.io/lab3-start/ex1.html):  Dense Matrix-Vector Multiply:  Optimizing serial code, Memory access paterns, Benchmarking
- [Exercise 2](https://psuastro528.github.io/lab3-start/ex2_nopycall.html): Benchmarking File I/O (no Python dependencies)
- [Exercise 2](https://psuastro528.github.io/lab3-start/ex2.html):  Benchmarking File I/O (& Calling Python Packages)
<br>
{{%/excerpt%}}

## Lessons / Resources
- Details for this class
   - [Getting Started with Julia on ACI](/tips/aci)
   - [Starting & Submitting Assignments](/tips/submitting)
- Julia
   - [Julia Manual](http://docs.julialang.org/en/v1/)
   - [Think Julia: How to Think Like a Computer Scientist](https://benlauwens.github.io/ThinkJulia.jl/latest/book.html)
   - [Learn Julia in Y Minutes](https://learnxinyminutes.com/docs/julia/)
- File Formats
   - [FITSIO library written in C](https://heasarc.gsfc.nasa.gov/fitsio/)
   - [HDF5](https://www.hdfgroup.org/solutions/hdf5/)
   - [Apache Arrow](https://arrow.apache.org/)
- Julia packages for reading files
   - Julia's [FileIO.jl](https://github.com/JuliaIO/FileIO.jl) high-level API
   - Julia's [JLD2.jl package](https://github.com/JuliaIO/JLD2.jl)
   - Julia's [HDF5.jl package](https://github.com/JuliaIO/HDF5.jl)
   - Julia's [FITSIO.jl package](https://github.com/JuliaAstro/FITSIO.jl)
   - Julia's [Apache [Arrow.jl](https://github.com/JuliaData/Arrow.jl) implementation
   - [Feather.jl](http://juliadata.github.io/Feather.jl/stable/)
   - [PyCall.jl documentation](https://github.com/JuliaPy/PyCall.jl#types).
- [Querying DataFrames](https://dataframes.juliadata.org/stable/man/querying_frameworks/)
   - [Query.jl](http://www.queryverse.org/Query.jl/stable/gettingstarted/)
   - [DataFramesMeta.jl](https://github.com/JuliaData/DataFramesMeta.jl))
   - [JuliaDB.jl](https://github.com/JuliaData/JuliaDB.jl)
- Miscelaneous
   - [Regular expressions in julia](https://docs.julialang.org/en/v1/manual/strings/index.html#Regular-Expressions-1)
   - [Astropy](http://docs.astropy.org)


{{% children depth="1" %}}
