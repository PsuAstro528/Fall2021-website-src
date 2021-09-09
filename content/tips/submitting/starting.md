+++
title = "Starting Labs"
course_inst = "Penn State"
course_number = "Astro 528"
course_name = "High-Performance Scientific Computing for Astrophysics"
weight = 0852

chapter= false
hidden = false

creatordisplayname = "Eric Ford"
creatoremail = "ebf11 at psu dot edu"
lastmodifierdisplayname = "Eric Ford"
lastmodifieremail = "ebf11 at psu dot edu"
+++

## Instructions for Starting Labs via ICS ACI Portal
1.  [Clone your Github Repository on ACI](#clone-repo) (only need to do once per assignment)
2.  [Open notebook](#open-notebook)
3.  [Save and commit changes as you go](#commit-changes)
---

<a id="clone-repo"></a>
### Clone your github repository to begin a new assignment

- Request a "**BYOE Jupyter server**" session via the [ACI portal](https://portal.aci.ics.psu.edu/) (see [getting started](aci/#start-jupyter))
- While waiting for it to start, let's get the url for the repo to be cloned.
    + If you haven't followed the link to create your repo for this week's assignment, do that now.  Following that link should trigger GitHub to create a private git repository named labN-GITHUBID (where N is the week number and GITHUBID is the GitHub username that you're logged in as at the time you follow the link).
    + Navigate to the github repository you'll be using in your browser.
    + Click _Clone or download_.
    + If it says "Clone with https", click "Use ssh".
    + Click the clipboard icon to copy the url onto your clipboard
- Return to your browser tab with "My Interactive Sessions".
- Hopefully, there's now a _Connect to Jupyter Server_ button. Click it.
- Go to the newly opened tab, you'll have a Jupyter Lab Server.
- If you don't see tiles for Python, Julia and Pluto Notebooks, then click _File.New_Launcher_.
- Find the _Terminal_ tile or in the menu system, _File.New.Terminal_.
- In the new terminal tab, clone your github repo by running

```shell
git clone REPO_URL  # where REPO_URL is what you'll paste from the clipboard
```
- Change into the directory that was created for the repository (we'll call REPO_DIR) and setup all the package dependencies required (as specified by the Project.toml or test/Project.toml file or embedded in Pluto notebooks).

<!-- (For people who are particularly interested in Julia's package manager:  Normally, this would be in the root directory, but I found having one broken mybinder.org's ability to install Julia packages successfully.  So putting the Project.toml in the test directory is a work around for repositories that don't need to become a Julia package.  That proved to create some problems with travis, so starting with Lab 4, I'm reverting to putting the Project.toml in the root directory.)  -->

<!-- Labs 1-3: -->
<!--
```shell
cd REPO_DIR
julia --project test -e 'using Pkg; Pkg.instantiate(); '
```
Labs >=4:
-->
```shell
cd REPO_DIR
julia --project -e 'using Pkg; Pkg.instantiate(); '
```

- Optional (can do later if needed):  In case the instructor makes changes to the template, it would be useful to be able to merge in those changes easily.  To prepare for that, let's set a remote upstream repository.  Here I assume that your REPO_URL was https://github.com/GITHUBID/example-GITHUBID.git.  Notice that we're replacing the first GITHUB id by the organization name "PsuAstro528" and remove the "-GITHUBID" at the end.
```shell
git remote add upstream git@github.com:PsuAstro528/example.git
```

Unfortunately, Pluto notebooks can be a bit finicky.  So in many cases it may make more sense to just download the replacement notebook from the starter repository and overwrite your.

If you did want to attempt to merge changes from the starting repository (e.g., for files other than Pluto notebooks), then you can run either
```shell
git pull upstream main
```
or if you have a newer version of git
```shell
git pull upstream main --allow-unrelated-histories
```

---
<a id="open notebook"></a>
### Open notebook

- Go back to the browser tab with your Jupyter Lab server running.
- If you do not see the tiles for Python, Julia and Pluto, then go to File.New_Launcher.
- If the lab contains Pluto notebooks (most lab exercises ending in .jl), then
   + Click the Pluto tile.  A new tab will open in your browser for the Pluto session.
   + In the "Open from file" box, type the path to the directory containing the repo, a forward slash and the name of the first notebook (e.g., 'lab1-yourgithubid/ex1.jl').  Tab completion is often helpful.
- If the lab contains Jupyter notebooks (files ending in .ipynb), then:
   + Click the directory name of the repository that you just installed.  (If you don't see a list of files on the left, then click the Folder icon in the upper left.)
   + Double click on the name of the Jupyter notebook file (e.g., ex1.ipynb)
   + A new tab within the JupyerLab browser tab will open with the Jupyter notebook.
- Do your work in the notebook.
- When you're done with a notebook, make sure it is saved (Ctrl+S) and close the tab.

---
<a id="commit-changes"></a>
### Commit your changes
Ideally, you'd commit small changes as you go.  At a minimum, make sure that you [commit your changes](../commit) each time you are wrapping up a coding session or about to take a break.
