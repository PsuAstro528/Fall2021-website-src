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
[Lab 3: **Memory Hierarchy: Cache, RAM, Disk I/O, File formats**](https://github.com/PsuAstro528/lab3-start) (due Sept 16)
<br />
- [Exercise 1](https://psuastro528.github.io/lab3-start/ex1.html): Dense Matrix-Vector Multiply
- [Exercise 2](https://psuastro528.github.io/lab3-start/ex2.html): Benchmarking File I/O (& Calling Python Packages)
<!-- - Exercise 2: DataFrames, Join, Query -->
<br>
<!--
[Lab 3 Git Repository](https://github.com/PsuAstro528/lab3-start)
- [Exercise 1: Benchmarking File I/O & Calling Python Packages](https://nbviewer.jupyter.org/github/PsuAstro528/lab3-start/blob/master/ex1.ipynb)
- [Exercise 2: DataFrames, Join, Query](https://nbviewer.jupyter.org/github/PsuAstro528/lab3-start/blob/master/ex2.ipynb)
- [Exercise 3: Dense Matrix-Vector Multiply](https://nbviewer.jupyter.org/github/PsuAstro528/lab3-start/blob/master/ex1.ipynb)
-->
{{%/excerpt%}}

## Lessons / Resources
- Julia, general
   - [Julia Manual](http://docs.julialang.org/en/v1/)
   - [Think Julia: How to Think Like a Computer Scientist](https://benlauwens.github.io/ThinkJulia.jl/latest/book.html)
   - [Learn Julia in Y Minutes](https://learnxinyminutes.com/docs/julia/)
   - [FITSIO library written in C](https://heasarc.gsfc.nasa.gov/fitsio/)
   - [HDF5](https://www.hdfgroup.org/solutions/hdf5/)
   - [Apache Arrow](https://arrow.apache.org/)
- Julia packages for reading files
   - Julia's [FileIO.jl](https://github.com/JuliaIO/FileIO.jl) high-level API
   - Julia's [JLD2.jl package](https://github.com/JuliaIO/JLD2.jl)
   - Julia's [HDF5.jl package](https://github.com/JuliaIO/HDF5.jl)
   - Julia's [FITSIO.jl package](https://github.com/JuliaAstro/FITSIO.jl)
   - Julia's [Apache Arrow.jl](https://github.com/JuliaData/Arrow.jl) implementation
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
