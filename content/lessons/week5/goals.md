+++
title = "Learning goals"
course_inst = "Penn State"
course_number = "Astro 528"
course_name = "High-Performance Scientific Computing for Astrophysics"
weight = 05103  #wwdpp

chapter= false
hidden = false

creatordisplayname = "Eric Ford"
creatoremail = "ebf11 at psu dot edu"
lastmodifierdisplayname = "Eric Ford"
lastmodifieremail = "ebf11 at psu dot edu"
+++

# Week 5
{{%excerpt%}}
- Exercises
   - Profile code
   - Identify type instability via code inspection macros
   - Identify opportunities for optimziation
      - Writing type stable functions
      - Optimize performance by reducing memory allocaitons
   - Optimize code for serial execution
- Project
   - Profile code to identify code worth optimizing
   - Document code to increase chances of useful feedback from peer code review
{{%/excerpt%}}

## Lessons along the way
- Type stability: [`@code_warntype`](https://docs.julialang.org/en/v1/manual/performance-tips/#man-code-warntype), [JETTest.jl](https://aviatesk.github.io/JETTest.jl/dev/)
- Performance impact of `global`'s
- Strict typing, sub-types, union types
