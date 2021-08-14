+++
title = "Committing changes"
course_inst = "Penn State"
course_number = "Astro 528"
course_name = "High-Performance Scientific Computing for Astrophysics"
weight = 0853

chapter= false
hidden = false

creatordisplayname = "Eric Ford"
creatoremail = "ebf11 at psu dot edu"
lastmodifierdisplayname = "Eric Ford"
lastmodifieremail = "ebf11 at psu dot edu"
+++


- Make sure you've saved all your changes (Ctrl+S)
- To commit changes to a single file:
```shell
git add ex1.jl
git commit -m "note describing this change"
```
- To commit your work on all files beginning with ex:
```shell
git add ex*
git commit -m "note describing these changes"
```
