# Human-Computer Interaction Final Project: Prototype Design and Research Project

<https://smcclab.github.io/thirty-nine-hundred-hci/assessments/03-prototype-and-evaluation.html>

This repository is to submit the Final Project: Prototype Design and Research Project from Human-Computer Interaction, COMP3900/6390.

If you're a student in this class, there are a few things you need to do to get started.

## To start

1. fork this project to your own "uid" [GitLab](https://gitlab.comp.anu.edu.au/) account

2. when you fork it, make sure that you don't change the name

3. when you fork it, make sure that the visibility level of the project remains "private", our marker user is added automatically.

## For the assignment

1. Read the assignment specification carefully.

2. Follow appropriate prototyping, data gathering and analysis processes to address the research challenge.

3. Evaluate your prototype with 3--5 participants: all participants must be current COMP3900/6390 students, and you must list them in the _Participants_ section of your documentation in the exact format shown in the template (`- u1234567 Firstname Lastname`). A CI/CD job checks the format, and after the deadline the course staff verify the uids and names against the class list, cross-check them against every other submission, and contact a random sample of listed participants to confirm they took part.

4. Upload your **raw** research data (e.g., exported survey or questionnaire responses with timestamps, session recordings or photographed notes, and verbatim transcripts) as well as analysis scripts and other relevant files in the `materials` directory of your fork of this template repository. Summaries or aggregated tables are not a substitute for the raw data.

5. Write your project documentation in `project-documentation.md` following the headings provided in the template. Use proper markdown syntax to format your document and display images.

6. Record your presentation and upload it as `project-presentation.mp4` in the top level of your fork. The video must be in `.mp4` format (h.264 or h.265 encoding), no larger than 1920x1080 pixels, and no longer than 330 seconds (5 minutes + 10% buffer). Your presentation video is the primary document for marking purposes. The video file must be **under 100MB**: see [Exporting and compressing your video](#exporting-and-compressing-your-video) below **before you commit it**.

7. Don't forget to include at least five references to external sources in your documentation: a numbered Markdown list in ACM reference format, each entry ending with a working DOI or URL, and each cited in your text by number, e.g. `[1]`. The References section of `project-documentation.md` has the full rules and example entries.

8. commit and **push** your changes to GitLab

9. wait for the CI/CD jobs to complete (click "Build" and then "Jobs" in the left sidebar), you should see all green ticks. The video check jobs will tell you if your presentation video is missing, too long, or too large. The word count, markdown, and participants checks run even if you haven't uploaded your video yet.

_Note_: you can push as many times as you like and all versions are backed up on GitLab with the time and date that you pushed it. Push early and push often.

## Exporting and compressing your video

Your `project-presentation.mp4` (and any recordings in `materials`) must be under 100MB so it can be pushed normally. Please do not use Git LFS. Git keeps every version you commit, so a file that is too large stays in your repository even after you replace it with a smaller one: check the size **before** you `git add` it.

1. **Export from PowerPoint at Full HD (1080p)**: File → Export → Create a Video → Full HD (1080p). Don't choose Ultra HD (4K), which is larger than the 1920x1080 limit. Name the file `project-presentation.mp4`.

2. **Check the file size**: Get Info (macOS), Properties (Windows), or `ls -lh project-presentation.mp4`.

    - **Under 100MB:** you're done. Commit and push it as it is.
    - **100MB or more:** re-encode it with the settings in step 3 before you commit it.

3. **Only if your video is 100MB or more, re-encode it to H.264 at 2000 kbps with 128 kbps AAC audio.** These settings give about 88MB for a 330-second video and still look sharp for slides and your face. Use either:

    - [HandBrake](https://handbrake.fr) (free, with a graphical interface): open your exported video, choose the **Fast 1080p30** preset, then on the **Video** tab select **Avg Bitrate (kbps)**, enter `2000`, and tick **Multi-Pass Encoding**. Save the output as `project-presentation.mp4`.
    - [ffmpeg](https://ffmpeg.org) (command line), after renaming your PowerPoint export to `exported-video.mp4`:

        ```sh
        ffmpeg -i exported-video.mp4 -c:v libx264 -preset slow -b:v 2000k -maxrate 2500k -bufsize 5000k -pix_fmt yuv420p -c:a aac -b:a 128k -movflags +faststart project-presentation.mp4
        ```

    Check the size of the new file again, and watch it through once to make sure the audio and video are fine.

## Help with GitLab and Markdown

If you are having trouble with GitLab or Markdown, we have resources available on the course Canvas site, and you can go straight to the course forum and ask questions at any time for help with these technologies.

The short version is:

- **GitLab:** have a look at this page <https://comp.anu.edu.au/docs/gitlab/>
- **Markdown:** read this website <https://www.markdownguide.org>

**Markdown Formatting Check:** There is a CI/CD job that checks your markdown formatting using the [`markdownlint-cli`](https://github.com/igorshubovych/markdownlint-cli) tool. Syntax rules are listed in the [markdownlint rules documentation](https://github.com/DavidAnson/markdownlint/blob/main/doc/Rules.md); in our script, rules `MD004` (so you can mix `*` and `-` list markers), `MD013` and `MD041` are disabled. All other rules are active.

## Getting help

If you have any questions or problems, ask in consultation time after your tutorial or on the course forum.
