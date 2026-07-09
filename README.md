# Human-Computer Interaction Final Project: Prototype Design and Research Project

<https://smcclab.github.io/thirty-nine-hundred-hci/assessments/03-prototype-and-evaluation.html>

This repository is to submit the Final Project: Prototype Design and Research Project from Human-Computer Interaction, COMP3900/6390.

If you're a student in this class, there are a few things you need to do to get started.

## To start

1. fork this project to your own "uid" [GitLab](https://gitlab.cecs.anu.edu.au/) account

2. when you fork it, make sure that you don't change the name

3. when you fork it, make sure that the visibility level of the project remains "private", our marker user is added automatically.

## For the assignment

1. Read the assignment specification carefully.

2. Follow appropriate prototyping, data gathering and analysis processes to address the research challenge.

3. Upload research data and analysis scripts as well as other relevant files in the `materials` directory of your fork of this template repository.

4. Write your project documentation in `project-documentation.md` following the headings provided in the template. Use proper markdown syntax to format your document and display images.

5. Record your presentation and upload it as `project-presentation.mp4` in the top level of your fork. The video must be in `.mp4` format (h.264 or h.265 encoding), no larger than 1920x1080 pixels, and no longer than 330 seconds (5 minutes + 10% buffer). Your presentation video is the primary document for marking purposes.

6. Don't forget to include at least five references to external sources in ACM format in your documentation.

7. commit and **push** your changes to GitLab

8. wait for the CI/CD jobs to complete (click "Build" and then "Jobs" in the left sidebar), you should see all green ticks. The video check jobs will tell you if your presentation video is missing, too long, or too large.

_Note_: you can push as many times as you like and all versions are backed up on GitLab with the time and date that you pushed it. Push early and push often.

## Help with GitLab and Markdown

If you are having trouble with GitLab or Markdown, we have resources available on the course Canvas site, and you can go straight to the course forum and ask questions at any time for help with these technologies.

The short version is:

- **GitLab:** have a look at this page <https://comp.anu.edu.au/docs/gitlab/>
- **Markdown:** read this website <https://www.markdownguide.org>

**Markdown Formatting Check:** There is a CI/CD job that checks your markdown formatting using the [`markdownlint-cli`](https://github.com/igorshubovych/markdownlint-cli) tool. Syntax rules are listed in the [markdownlint rules documentation](https://github.com/DavidAnson/markdownlint/blob/main/doc/Rules.md); in our script, rules `MD013` and `MD041` are disabled. All other rules are active.

## Getting help

If you have any questions or problems, ask in consultation time after your tutorial or on the course forum.

## Note on PDF generation

This repository automatically generates a PDF file from your markdown document to create a nice version of your assessment document.

This is controlled by scripts in the `.gitlab-ci.yml` file.

Sometimes this process doesn't work the way you might expect so if you notice something wrong or unexpected in the artefact PDF, ask on the course forum.

In particular, due to how the Pandoc tool generates a PDF (using LaTeX), images float to where they fit in the document. If you have a lot of images in one place, they may float to the end of the document. This behaviour is acceptable but you should make sure that you refer to your images in your text (E.g., "The distribution of responses to the SUS survey is shown in Figure 1").
