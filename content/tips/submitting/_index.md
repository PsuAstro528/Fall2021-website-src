+++
title = "Starting & Submitting Assignments"
course_inst = "Penn State"
course_number = "Astro 528"
course_name = "High-Performance Scientific Computing for Astrophysics"
weight = 0850

chapter= false
hidden = false

creatordisplayname = "Eric Ford"
creatoremail = "ebf11 at psu dot edu"
lastmodifierdisplayname = "Eric Ford"
lastmodifieremail = "ebf11 at psu dot edu"
+++

## Need to update this page for Fall 2021

## Instructions for Completing Labs via ICS ACI Portal
1.  [Clone your Github Repository on ACI](#clone-repo) (only need to do once per assignment)
2.  [Commit your changes](#commit-changes)
3.  [Test your code](#test-code)
4.  [Commit your work and push to Github](#commit-push)
5.  [Submit your work via Github pull request](#submit-pr)
6.  [Review the feedback on your submission](#discuss-pr)

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

- Go back to the browser tab with your Jupyter Lab server running.
- Click the directory name of the repository that you just installed.
- Open a Pluto (files ending in .jl) or Jupyter (files ending in .ipynb) notebook in that repo.
- Do your work in the notebook.
- When you're done with a notebook, make sure it is saved (Ctrl+S) and close the tab.

---
<a id="commit-changes"></a>
### Commit your changes
Ideally, you'd commit small changes as you go.  At a minimum, make sure that you commit your changes each time you are wrapping up a coding session or about to take a break.
- To commit changes to a single file
```shell
git add ex1.jl
git commit -m "note describing this change"
```
- To commit your work on all files beginning with ex,
```shell
git add ex*
git commit -m "note describing these changes"
```

---
<a id="run-tests"></a>
### Test your code

- Make sure you've committed all your changes (including adding any new files)
- Check that your code passes any tests embedded in each notebook as you go.  
- To test a single exercise, you can use a terminal window to run
```julia
julia --project test test/test1.jl
```
- To test al the exercises, you can run
```julia
julia --project test test/runtests.jl
```
<!-- in a separate test notebook like test_myself.ipynb:

```julia
using NBInclude
@nbinclude("exercise1.ipynb")
include("test/test1.jl")
```
- If using a Jupyer notebook, if you make changes and retest, then restart the kernel for the test notebook to be sure there aren't unintended carryover effects.
- Once you think you're done, you are encouraged to test your full repository even more similarly to how it will be tested by the continuous integration testing by opening a terminal window and running `julia test/runtests.jl`
-->

---
<a id="convert-to-markdown"></a>
### Convert any Jupyter notebooks to Markdown

- You'll skip this step for any assignments that are Pluto notebooks, since Pluto notebooks are already valid Julia code.
- Return to the terminal tab # (or open a new one)
- Run the following commands
```shell
cd YOUR_REPO_DIRECTORY     # You'll need to replace YOUR_REPO_DIRECTORY and NOTEBOOK_NAME
julia --project=. -e 'using Weave; convert_doc("NOTEBOOK_NAME.ipynb","NOTEBOOK_NAME.jmd")'
git add NOTEBOOK_NAME.jmd  # Only need to do this once per new file you create if you use the -a option with "git commit" below.  Otherwise, need to do each time you want to deposit a new version of the file into your respository.
```

---
<a id="commit-push"></a>
### Commit your changes and push to Github

- Return to the terminal tab (in YOUR_REPO_DIRECTORY)
- Run the following commands

```shell
git commit -a -m "Completed"    # Commit all changes you've made to files being tracked and lets me know that you're done with the assignment
git push                        # Uploads your progress to github
```

<!--
- If this repository is configured to apply tests via continuous integration, then navigate to your repository, click ACtions, then look for "Workflows" and choose "Test notebooks".  There will be some tests of early versions that have red x's next to them.  Hopefully, your latest submission (typically at the top of the list) will have a green checkbox next to it.  If not, then you can click on that commit string, then click "test (...)" and see the results of the continuous integration tests.
-->

- When you're all done, close browser tabs and remember to go back to the "My Interactive Sessions" tab in the ACI Portal, click "Delete" for this Sessions and confirm.

---
<!---

<a id="submit-pr"></a>
### Submit your work via Github pull request

- Make sure you've committed all your changes
- Check that your code passes all the tests (or as many as practical in time avaliable)
- Navigate to your github repository for the assignment
- Click _New Pull Request_ button (second button from left, below the orange bar)
- Set the left button to "base:original".  Leave the right button "compare:master".
- Review the updates to the page and make sure this is the version you intend to submit.
- Enter a name for the pull request in the text box to the right of your avitar/icon.
- Optionally, write a longer messages in the larger box below
- Click _Create Pull Request_

-->

---
<a id="discuss-pr"></a>
## Review the feedback on your submission
- Browse to your github repository.
- GitHub classroom opens a pull request for each assignment automatrically
- Click _Pull Requests_, then click on _Feedback_, the name of the pull request that GitHub classroom created for us.
- In the "Checks" tab, click "Test notebook".  If there's a red x next to the "test (...)" job, then click on it to see the results of the continuous integration testing.  This should happen several minutes after you push your changes.
- If you notice a problem that you'd like to fix, then you can make, commit and push more changes.
- In the Conversations tab (default), you and the instructor can discuss the pull request in general using the text box at the bottom of the page.
- In the "Files changed" tab, the instructor can provide comments on specific lines of your submission.  

