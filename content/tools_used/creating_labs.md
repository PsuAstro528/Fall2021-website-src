+++
title = "Creating lab assignments"
course_inst = "Penn State"
course_number = "Astro 528"
course_name = "High-Performance Scientific Computing for Astrophysics"
weight = 1100
include_toc = true

creatordisplayname = "Eric Ford"
creatoremail = "ebf11 at psu dot edu"
lastmodifierdisplayname = "ebf11 at psu dot edu"
lastmodifieremail = "ebf11@psu.edu"
+++

# Workflow for creating lab assignments

### Create Development repostiory on GitHub:
   - Create an empty _private_ repository named labN-dev at GitHub.
      + Go to the [class organization page at GitHub](https://github.com/PsuAstro528), click New
      + Repository Name: labN-dev
      + Description: Lab N
      + Private
      + Uncheck Initialize README, .gitignore: None, License: None
      + Create repository- Change into directory of lab exercises

### Create local development repository 
- Change into directory of lab exercises `cd ~/Teach/Astro528/Fall2021/exercises`
- Create new Julia package with Project.toml file for the lab and add common packages.
```julia
using Pkg
Pkg.generate("labN")
Pkg.activate("labN")
Pkg.add(["InteractiveUtils","Markdown","PlutoUI","PlutoTeachingTools","LaTeXStrings"])
```

- Add template files from template repository (lab-template) into labN-dev directory
```shell
mv labN labN-dev
cd labN-dev
cp -r ../lab-template/* .
cp -r ../lab-template/{.gitignore,.github} .
```
### Make local repository and commit template files 

```shell
git init
git add .gitignore .github docker-compose.yml environment.yml LICENSE README.md src test
git commit -m "template"
```

### Rename to use main branch, connect to remote repo and push to GitHub
```shell
git branch -m master main
git remote add origin git@github.com:PsuAstro528/labN-dev.git
git push -u origin main
```

### Create & Switch to solution branch
```shell
git checkout -b solution
```
### Make exercises (named exN.jl or exN.ipynb) and tests (named test/testN.jl)
   - Indicate code to be removed with missing in Pluto notebooks, so its easy to find.  
   - For Jupyter notebooks add comment SOLUTION.

```shell
git add ex?.jl ex?.ipynb test/test?.jl
git commit -m "new exercise"
```
### Setup test directory
Once assignments is ready for continuous integration testing, create/update the Project.toml file in test directory to include needed packages:
   - `julia -e 'using Pkg; Pkg.activate("test"); Pkg.add(["Test","InteractiveUtils","Markdown","PlutoUI","PlutoTeachingTools","LaTeXStrings"])'`
   - Add any other packages required by any notebook to test/Project.toml
   - Test each exercise as you go:  `julia --project=test -e 'include("test/test1.jl")'`
   - Test as a group:  `julia --project=test -e 'include("test/runtests.jl")'`


- Add Project.toml to the repo and make remote solution branch track local solution branch
```shell
git add test/Project.toml test/test?.jl
git commit -m "tests for exN"
git push -u origin solution`
```

### Check solution passes CI testing

Check status of tests from Github Actions tab https://github.com/PsuAstro528/labN-dev/actions .


### Make Julia Markdown version of solutions

- Once it passes CI tests and you're ready to share, use Weave package to convert any Jupyter notebooks into jmd files.

```shell
julia -e 'using Weave; convert_doc("ex1.ipynb","ex1.jmd");'
julia -e 'using Weave; convert_doc("ex2.ipynb","ex2.jmd");'
julia -e 'using Weave; convert_doc("exN.ipynb","exN.jmd");'
```

- Add and commit exN.jl and exN.jmd to solution branch

```shell
git add ex?.jl ex?.jmd; git commit -m "convert from ipynb"
```

- Checkout main branch and add notebook, Project and test files from solution branch.
```shell
git checkout main
git checkout solution exN.jl
git checkout solution exN.jmd
git checkout solution test/testN.jl
git checkout solution Project.toml
git checkout solution test/Project.toml
```

- Edit each exN.jl and/or exN.jmd to remove code
   - Search for SOLUTION and remove code not for students to see
   - (Note to future self: Should I automate this?)
   - Recreate any cleaned Jupyter notebook files exN.ipynb

```shell
julia -e 'using Weave; convert_doc("ex1.jmd","ex1.ipynb");'
julia -e 'using Weave; convert_doc("ex2.jmd","ex2.ipynb");'
julia -e 'using Weave; convert_doc("exN.jmd","exN.ipynb");'
```

   - Check that you're happy with the resulting notebooks, then add & commit them to main branch.

```shell
git add ex?.jl ex?.jmd ex?.ipynb test/test?.jl
git commit -m "cleaned ex"
git push
```

### Create Starer Repository for Students
Create starter repostiory on GitHub.com from development repository

   - Create an empty public lab named labN-start at GitHub as part of the organization for the class.
      + Go to https://github.com/PsuAstro528, click New
      + Description: Lab N:  List super-short lesson goals
      + Public
      + Uncheck Initialize README, .gitignore: None, License: None
      + Create repository
   - Change into directory of lab exercises `cd ~/Teach/Astro528/Fall2021/exercises`
   - `cp -r labN-dev labN-start`
   - `cd labN-start`
   - Make _sure_ you're in the labN-start subdirectory
   - `rm -rf .git`
   - `git init`
   - `git remote add origin git@github.com:PsuAstro528/labN-start.git`
<!--   - Edit .travis.yml to no longer just test solution and now exclude original branch -->

```shell
git add *
git add .gitignore .github # .travis.yml
git commit -m "init"
git branch -m master main
git push --set-upstream origin main
```

Make original branch for comparison purposes and switch back to main branch
```shell
git checkout -b original
git push -u origin original
git checkout main
```

Check that you're happy with the labN-start repository

### Distribute new laboratory assignment
Go to https://classroom.github.com/classrooms

   - Choose class
   - New Assignment
   - Create an Individual Assignment
      -  Title: Astro 528 Lab N
      -  Repo prefix: labN
      -  Private
      -  Enable assignment invitation URL
      -  Add your starter code from GitHub:  https://github.com/PsuAstro528/labN-start
      - Deadline: Sunday 23:59pm
      - Create Assignment
   -  Copy Invitation Link and send it to students in a Canvas announcement
