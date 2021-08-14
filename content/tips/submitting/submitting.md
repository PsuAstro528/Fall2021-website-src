+++
title = "Submitting Labs"
course_inst = "Penn State"
course_number = "Astro 528"
course_name = "High-Performance Scientific Computing for Astrophysics"
weight = 0857

chapter= false
hidden = false

creatordisplayname = "Eric Ford"
creatoremail = "ebf11 at psu dot edu"
lastmodifierdisplayname = "Eric Ford"
lastmodifieremail = "ebf11 at psu dot edu"
+++

1.  [Commit your changes](#commit-changes)
2.  [Convert any Jupyter notebooks to Markdown](#convert-to-markdown)
3.  [Commit your work and Push to Github](#commit-push)
4.  [Review the feedback on your submission](#discuss-pr)

---

<a id="commit-changes"></a>
### Before you submit
Ideally, you'd commit small changes as you go.  At a minimum, make sure that you [commit your changes to your local repository](../commit) each time you are wrapping up a coding session or about to take a break.
Consider [testing your code](testing) on ACI (or you local computer) before submitting the final version of your code.

---
<a id="convert-to-markdown"></a>
### Convert any Jupyter notebooks to Markdown

- You'll skip this step for any assignments that are Pluto notebooks, since Pluto notebooks are already valid Julia code.
- Return to the terminal tab (or open a new one) and make sure you're in your repo's directory

- Run the following commands
```shell
julia --project=. -e 'using Weave; convert_doc("NOTEBOOK_NAME.ipynb","NOTEBOOK_NAME.jmd")'
git add NOTEBOOK_NAME.jmd  # Only need to do this once per new file you create if you use the -a option with "git commit" below.  Otherwise, need to do each time you want to deposit a new version of the file into your respository.
```

---
<a id="commit-push"></a>
### Commit your changes and push to Github
- Return to the terminal tab, make sure you're in your repo's directory.
- Run the following commands

```shell
git commit -a -m "Completed"    # Commit all changes you've made to files being tracked and lets me know that you're done with the assignment
git push                        # Uploads your progress to github
```

<!--
- If this repository is configured to apply tests via continuous integration, then navigate to your repository, click ACtions, then look for "Workflows" and choose "Test notebooks".  There will be some tests of early versions that have red x's next to them.  Hopefully, your latest submission (typically at the top of the list) will have a green checkbox next to it.  If not, then you can click on that commit string, then click "test (...)" and see the results of the continuous integration tests.
-->

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
