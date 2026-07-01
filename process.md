# JSDSS Author Submission and Review Process

## 1. Author Submission

- Create a new repo in **your** GitHub account using the template repository: [`jsds-sports/jsdss-manuscript-template`](https://github.com/jsds-sports/jsdss-manuscript-template).
    - Go to: <https://github.com/jsds-sports/jsdss-manuscript-template>
    - Click **Use This Template** in the upper right.
    - Toggle **Include All Branches** on.
    - Give the repo a reasonable name of your choice.
    - You may choose to change the visibility to **Private** while working on the project.
    - Click **Create Repo**.
- Clone repo to your machine.
- Write paper with code and data.
- Submit PDF to the OJS system at Charlotte.

## 2. *JSDSS* Review Process

- An editor and multiple reviewers read the PDF.
- If there is sufficient interest in potentially publishing the paper, we invite the author to submit for a reproducibility review.
    - The author is responsible for putting the paper contents in our Quarto format (as laid out in the template repo).
    - The GitHub Actions script that is already part of the template needs to execute correctly. This will be executed automatically when the author pushes changes to the repo on GitHub.
- Upon successful rendering via GitHub Actions in the **author's** repo, the reproducibility editor **forks** the author's repo into the `jsds-sports` GitHub Organization.
    - At this point, the author should create a [**release**](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases) at the time the repo is forked.
    After it is forked, the author also makes the repo public (perhaps temporarily), to give the Editors Change Visibility permissions when the article is ready to be published. The Editors won't change Private to Public until final publication. If the author doesn't want the repo to be public yet, they can immediately Change Visibility to Private again. Otherwise, the author can leave it as Public.
    - *JSDSS* editors go to Settings and **we should go to Org settings and change these things there because we want them to apply to all repos by default.**
        - Rename the repo to match the OJS paper ID tracking system (e.g., `2026-baumer-413`).
        - Enable Issues
        - Protect main branch 
        - Invites Authors as collaborators with direct access and **Write** permissions 
        - Create an `R0` release in the forked repo.
    - (Needed one private, not needed one public. ) Editor goes to **Settings → Pages** and, in the branch section, chooses `gh-pages`.
    - (Maybe remove, so say to check it runs automatically. It Auto ran when it was public, but does not auto run when it's private. ) Editor goes to **Actions**, selects **Quarto Publish** on the left, and selects **Run Workflow** on the right to confirm GitHub Actions has no problems.
    - (Maybe remove) Author adds the `jsds-sports/2026-baumer-413` repo as a `downstream` remote (via [`git remote`](https://git-scm.com/docs/git-remote)).  
    

## 3. *JSDSS* Reproducibility Review Process

- The GitHub Actions script that is already part of the template needs to execute correctly.
    - If that works, the paper data and code go to the reproducibility editor for review.
- **Major comments:** Editor collates comments from reviewers posted in OJS and creates [GitHub Issues](https://docs.github.com/en/issues/tracking-your-work-with-issues/learning-about-issues/about-issues) for more substantive feedback.
    - One Issue per major comment (could be from multiple reviewers).
    - One Issue for all typos and minor suggestions.
    - Editor assigns Issues to the author, reviewer, and themselves.
- **Minor edits:** At any time throughout this process, the reproducibility editor (and other reviewers) can send simple, non-controversial minor edits back to the author via a pull request from `jsds-sports/2026.baumer.736 reviewer1-edits` to `jsds-sports/2026.baumer.736 main` (using the suggestions feature).

## 4. Revision Phase

- Author will respond to GitHub Issues (can ask clarifications, push back, etc.) by commenting via the web interface.
- Author edits the original repo on their account.
    - Commits should be tagged to Issues.
- Author prepares a pull request to `jsds-sports/2026-baumer-413 main` and can send commits to this branch as they see fit.
    - Author creates a Pull Request from the JSDSS repo (may need to **Change Base**).
    - Author ensures that all Issues are addressed in the pull request.
- When the author is done, the author tags the Editor to review the pull request.
    - If the GitHub Actions script works, the Editor merges the pull request and creates an `R1` release.

## 5. Repeat Steps 3 and 4

- Repeat the reproducibility review and revision phases until the Editor is satisfied.

## 6. Production Phase

- Author signs copyright forms.
- Editor creates a `final` release and the repo is frozen.
- GitHub Pages is turned **ON** and the paper is available in HTML/PDF/Word formats at `https://jsds-sports.github.io/2026-baumer-413/`.
- Editor obtains a DOI for the paper.
- Editor adds watermark and logo to the paper for authenticity.
- Editor adds that URL and paper metadata to the `jsds-sports.github.io` main website.
- Editor adds PDF of the paper to Project Euclid.
- Paper is now available via Project Euclid and the GitHub Pages site.
