+++
title = "Grading Rubrics"
course_inst = "Penn State"
course_number = "Astro 528"
course_name = "High-Performance Scientific Computing for Astrophysics"
weight = 590

creatordisplayname = "Eric Ford"
creatoremail = "ebf11 at psu dot edu"
lastmodifierdisplayname = "Eric Ford"
lastmodifieremail = "ebf11 at psu dot edu"
+++

## Class Project
The class project consists of several parts, each of which has its own submission deadline.  It is particularly important that you provide code for peer review on time, so that your peer reviewer is able to provide thoughtful and helpful feedback in time for it to improve your code for the latter parts of the project.  The project grade will be based on:

### Project Components
- [Project Proposal](#project-proposal) (5 points)
- Checkpoint 1: [Serial version of code](#serial-version-of-code) (10 points)
- Checkpoint 2: [Multi-core version of code](#first-parallel-version-of-code) (10 points)
- [Peer code reviews](#peer-code-reviews) (5 points)
- Checkpoint 3: [Distributed-memory/GPU/TPU/Cloud version of code](#second-parallel-version-of-code) (10 points)
- Final Submission: [Completed project code with documetation, benchmarking results and summary of lessons learned.](#final-submission) (5 points)
- [Project Presentation](#project-presentation) (5 points)

The grading rubric for each part of the proposal is provided below.


### Project Proposal

{{%excerpt-include filename="project/proposal.md" /%}}

### Serial version of code

{{%excerpt-include filename="project/serial.md" /%}}

### Peer Code Reviews

{{%excerpt-include filename="project/code_reviews/rubric.md" /%}}

For more information, see [instructions for code review](/project/code_reviews).

### First parallel version of code
Typically, the first parallel version runs on multiple cores using a shared memory system.

{{%excerpt-include filename="project/parallel1.md" /%}}

### Submit second parallel version of code
Typically, the second parallel version of the code is parallelized using one of: multiple cores with distributed-memory or a GPU.  Other alternatives include using Intel Phis, TPUs, or a cloud environment like JuliaHub.

{{%excerpt-include filename="project/parallel2.md" /%}}

### Completed Project:
{{%excerpt-include filename="project/final_submission.md" /%}}

### Project Presentation
{{%excerpt-include filename="project/presentations.md" /%}}
