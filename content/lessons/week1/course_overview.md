+++
title = "Course Overview (slides)"
date = "15 Jul 2021"
course_inst = "Penn State"
course_number = "Astro 528"
course_name = "High-Performance Scientific Computing for Astrophysics"
weight = 01103  # wwdpp

chapter= false
hidden = false

creatordisplayname = "Eric Ford"
creatoremail = "ebf11 at psu dot edu"
lastmodifierdisplayname = "Eric Ford"
lastmodifieremail = "ebf11 at psu dot edu"

type = "page"
theme = "psu"
[revealOptions]
transition= 'slide' # 'none','fade','concave','convex','zoom'
controls= true
progress= true
history= false
center= true
loop= false
pdfSeparateFragments= false
showNotes= true
+++


{{<revealjs theme="psu" transition="slide" controls="true" progress="true" history="false" center="false" loop="false" pdfSeparateFragments="false" showNotes="true" >}}
## Welcome
Penn State Astro 528

High-Performance Scientific Computing for Astrophysics

Eric Ford


---
## Safety & Respect
___
### University Policy
As of June 28, masks are optional for those who are fully vaccinated (two weeks after the second dose in a two-dose series or two weeks after a single-dose vaccine), including in classroom, advising, and student services spaces. Unvaccinated individuals must continue to wear masks indoors at all times.
___
### Please err on the side of caution
- If not feeling well, please stay home.
- If have reason to beleive may have been exposed, please stay home.
- Please let me know in advance (to the extent practical).
- Please work with me to make it practical for students to participate remotely when staying home to help protect others.
___
- Being extra cautious in class will help peers and instructor to focus on learning, rather than worrying about their safety.
- If engage in less safe activities outside of class, please take precautions.
___
###
---
## Course goals

Enhance your skills for scientific computing
- Increase your productivity
   + Choose right tool for right task
   + Reduce time debugging
   + Improve reproducibility
   + Increase impact of your software
- Enable you to
   + Analyze "Big Data"
   + Increase resolution of simulations
   + Include more complex physics

---
<!-- .slide: data-background="#093162" -->
### Course outline

- Software Development Practices
- Writing efficient serial code
- Parallelizing code efficiently
___
### Software Development Practices

Note:
Ask what students think of when they hear "software development practices".
___
### Software Development Practices
- Version control
<!-- .element: class="fragment" -->
- Testing & Continuous Integration
<!-- .element: class="fragment" -->
- Debugging
<!-- .element: class="fragment" -->
- Documenting & Literate Programming
<!-- .element: class="fragment" -->
- Coding standards
<!-- .element: class="fragment" -->
- Reviewing code
<!-- .element: class="fragment" -->
- Reproducibility
<!-- .element: class="fragment" -->
- Workflow
<!-- .element: class="fragment" -->

___
### Writing efficient serial code
- Processor architectures
- Memeory heirarchy
- Networking
- Programming languages
- Choosing algorithms
- Benchmarking
- Profiling
- Compilzer optimizations
- Optimizing
___
### Parallelizing code efficiently
- Shared-memory (e.g., one workstation)
- Distributed-memory (e.g., cluster)
- Accelerators
   + GPUs
   + TPUs (volunteers?)
- Cloud

Note:
Ask if any students already using parallel codes.  If so, how were they parallelized?
---
### Specific Objectives

- Increase technical knowledge
    + Readings, online lessons & class discussion
- Practice fundamentals on a small scalle
    + Lab/homework exercises
    + Make lots of mistakes quickly & learn from them
    + Make good habits routine
- Transfer skills into real work environment
    + Class project
    + Apply new skills to your research
    + Build deeper expertise in topics most relevant to you
    + Share what you learn with the class
___
### Readings, presentation
![textbooks](/images/textbooks.jpg)

___
### Readings, presentation
- Textbooks
   + _Writing Scientific Software: A Guide to Good Style_
   + _ThinkJulia: How to Think like a Computer Scientist_
   + _Introduction to High Performance Computing for Scientists and Engineers_ (definitely optional)
- Online PDFs
- Online tutorials
- Recordings?

Note:
Ask students if they would like to record classes.
Ask students if they like the idea of a pre-recorded lesson prior to class.
___
### Class discussions
- Let's learn from each other
- Introductions
   + Name
   + Department (if not Astro)
   + What skill you hope to strengthen through this course
---
<section id="setup">
## Let's get you set up
### Accounts
- Penn State
- [ICDS-ACI](https://ics.psu.edu/computing-services/account-setup/)
- [Github](https://github.com)

</section>
___
<section id="start">
### Get Started
For your first lab session, you'll:
- Follow link for lab 1 from Canvas announcement
- View _your_ new repository on [Github](https://github.com)
- Login to where you'll run your Jupyter notebooks (with Julia kernel)
   + [ICDS-ACI Portal](http://portal.aci.ics.psu.edu/)
   + [Install locally](https://julialang.org/downloads) (not for today)
- _Clone_ your "repo" for the lab
- Start working through ex1.ipynb, then ex2.ipynb

There are [more detailed instructions](../resources) on the website. 
<!-- about doing these using the [ICS-ACI Portal](http://portal.aci.ics.psu.edu/). -->
___
### Commiting Changes 

- Need to UPDATE for Fall
- _Commit_ your changes to local "repo"
- Can commit Pluto notebooks directly as .jl files.
- For Jupyter notebooks, first make a markdown version for human-readable version control 
  + Use Weave's convert_doc to conver Jupyter notebook (ex1.ipynb) into Julia Markdown (ex1.jmd)
  + Add & commit both ex?.ipynb and ex?.jmd files to your local repo
- Before signing off for the session, "push" your commits to GitHub
- When done with lab, create a _pull request_ to merge your work into the _branch_ named "original".

- See [more detailed instructions](lessons/week1/how-to-use-aci/#commit-push) &
  ask questions as you go
___
</section>

# Questions?
[Jump to start](#/0/0")

{{</revealjs>}}
