---
title: "JSDSS Author Submission and Review Process"
author: "JSDSS Editorial Board"
date: 2026-08-21
number-sections: true
---

Role-specific checklists: [authors](instructions-authors.md) · [reviewers](instructions-reviewers.md) · [associate editors](instructions-aes.md)

## Author Submission

### Prepare manuscript {#sec-prepare}

::: {.callout-tip}
**We strongly recommend the following workflow for authors.**
:::

- Create a new repo in **your** GitHub account using the template repository: [`jsds-sports/jsdss-manuscript-template`](https://github.com/jsds-sports/jsdss-manuscript-template).
    - Go to: <https://github.com/jsds-sports/jsdss-manuscript-template>
    - Click **Use This Template** in the upper right.
    - Toggle **Include All Branches** so that it is ON.
    - Give the repo a reasonable name of your choice.
    - You may choose to change the visibility to **Private** while working on the project.
    - Click **Create Repo**.
- Clone repo to your machine.
- Write paper with code and data. Use the Quarto template for the paper.
- Include a URL for the repo in the Acknowledgement section, or add editor as a collaborator to repo
- Generate PDF

::: {.callout-warning}

Alternatively, authors can choose to submit a PDF created in another manner. However, note that using [our template](https://github.com/jsds-sports/jsdss-manuscript-template) will eventually be required before publication if your manuscript proceeds along the review process and into the [GitHub review stage](#sec-github). 

:::

### Submit PDF

- Submit PDF to the [OJS system at Charlotte](https://journals.charlotte.edu/)

## *JSDSS* Initial Review Process

### Editor review

- An Editor will read the paper and determine if it is appropriate for *JSDSS*. 
    - If the paper is not appropriate, it will be **rejected** without further review. 
    - If the paper is appropriate, the Editor will assign an Associate Editor to handle the review.

### Associate Editor (AE) review

- An [Associate Editor](https://jsds-sports.github.io/#associate-editors) will read the paper and determine if it merits a full review in *JSDSS*. 
    - If the paper does not merit a full review, it will be **rejected** without further review. 
    - If the paper does merit a full review, the AE will assign **at least two** peer reviewers to read the PDF and submit their feedback in writing.
- The AE will combine the reviewers' feedback and their own and come to *exactly one* of the following recommendations:
    - **Reject**: The paper does not have a viable path to publication in *JSDSS*.
    - **Revise and resubmit**: The AE sees a path to publication, but the paper has substantive shortcomings that need to be addressed before any potential GitHub Review Process is initiated. 
    - **Invite to [GitHub Review Process](#sec-github-init)**: The AE sees a path to publication and wishes to initiate a deeper review. 
- The Editor will make a decision based on the AE's recommendation. 

::: {.callout-caution}

An invitation to the GitHub Review Process is **not** a conditional acceptance. 

:::

### Author decision

- Based on the Editor's decision and the AE and reviewer feedback, the author may choose to continue the review process, or withdraw the paper. 
- A decision of **Revise and resubmit** could occur more than once. 
- A decision of **Reject** or **Invite to GitHub Review Process** is terminal. 


## Initiation of GitHub Review {#sec-github-init}

- The author is responsible for creating a GitHub repository and putting the paper contents in *JSDSS* Quarto format, as described in @sec-prepare. The repo at this point should be private.
- The GitHub Actions script that is already part of the template needs to execute correctly. This will be executed automatically when the author pushes changes to the repo on GitHub.
- Upon successful rendering via GitHub Actions in the **author's** repo, the author invites the AE to the repo. 
- The AE **forks** the author's repo into the `jsds-sports` GitHub Organization. 

    - When forking, uncheck "Copy the main branch only". 
    - The journal fork must be **private** when it is created. The AE keeps it private for the duration of the internal review process and does not change it to Public until final publication.

- After it is forked, the author makes their own repo public (perhaps temporarily). This gives the AE the permissions to click the "Change Visibility" button in Settings on the journal fork. That permission will be used to make the journal repo public when the article is ready to be published.

    - If the author doesn't want their own repo to be public yet, they can immediately Change Visibility to Private again. Otherwise, the author can leave it as Public. 

- From this point on, all official reviews and edits will be done in the journal's version of the repo. The author is welcome to push changes to their personal repo as well, if desired. But all official issues, pull requests, etc., will occur in the journal's version of the repo. 
- AE goes to Settings page
    - General
        - Check that Change Visibility permissions are available. Otherwise, asks author to do the previous step.
        - Rename the repo to match the OJS paper ID tracking system (e.g., `2026-001-lastname-GHusername`).
        - Enable Issues 
        - The GitHub Actions script that is already part of the template needs to execute correctly. 
    - Collaborators and Teams
        - Invite Authors and Reviewers as collaborators with direct access and **Write** permissions
- AE goes to the main page of the journal fork and creates an `R0` [release](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases).

## *JSDSS* GitHub Review Process {#sec-github}

### Review phase {#sec-review}

- **Main comments:** AE collates comments from reviewers posted in OJS and creates [GitHub Issues](https://docs.github.com/en/issues/tracking-your-work-with-issues/learning-about-issues/about-issues) for more substantive feedback.
    - One Issue per main comment (could be from multiple reviewers).
    - One Issue for all typos and minor suggestions.
    - AE assigns Issues to the author, reviewer(s) that gave feedback related to that Issue, and themself.
- **Minor edits:** At any time throughout this process, the AE (and other reviewers) can send simple, non-controversial minor edits back to the author via a pull request from `jsds-sports/2026-001-lastname-GHusername reviewer1-edits` to `jsds-sports/2026-001-lastname-GHusername main` (using the suggestions feature).
    - Assign the author as **Assignee**. In this case the author is reviewing the AE's proposed edits, so also request the author's review. The AE still merges.

### Revision Phase {#sec-revise}

- Author will respond to GitHub Issues (can ask clarifications, push back, etc.) by comment via the web interface.
- Author edits the journal organization repo, not their own repo. 
    - Commits should be tagged to Issues.
- For each Issue, the author
    - Creates a new branch on the JSDSS repo `jsds-sports/2026-001-lastname-GHusername` to address that Issue, and makes edits on that branch.
    - Creates a pull request from the branch to `jsds-sports/2026-001-lastname-GHusername main` and can send commits to this branch as they see fit (may need to **Change Base**)
    - Ensures that all feedback from the Issue is addressed in the pull request.
- After the pull request is opened, the AE sets GitHub roles:
    - **Reviewers:** the peer reviewers for that Issue (not the authors).
    - **Assignees:** the authors. The AE assigns the lead author; the lead author may then assign a co-author if desired. 
- The author repeats for each Issue. If there are 5 Issues there will be 5 branches and 5 pull requests.
- If the GitHub Actions script works, all assigned Reviewers have approved, and the AE is satisfied, the AE merges the pull request. Otherwise, the review (@sec-review) and/or revision (@sec-revise) phases may be repeated until the AE is satisfied.
- After all pull requests are merged, AE creates an `R1` release.

Note that the following GitHub Settings are enabled by default: 

- Only AEs can merge PRs.
- Required Approvals is set to 1, but the AE should check that all Reviewers assigned to that PR have approved.
- If a commit is made after an approval has been given, that approval is stale and the PR needs to be re-approved by Reviewers

### Review and revise phase iteration

- AE makes *exactly one* of the following recommendations to Editor:
    - **Reject**: The paper has fatal flaws that prevent publication in *JSDSS*, and authors do not want to fix them.
    - **Accept**: The paper is ready for publication.
- The Editor will make a decision based on the AE’s recommendation.

## Production Phase

- Author signs copyright forms.
- Editor obtains a DOI for the paper.
- Editor adds watermark and logo to the paper for authenticity.
- Editor creates a `final` release and the repo is frozen.
- GitHub Pages is turned **ON** and the paper is available in HTML/PDF/Word formats at `https://jsds-sports.github.io/2026-001-lastname-GHusername/`.
- Editor adds that URL and paper metadata to the `jsds-sports.github.io` main website.
- Editor adds PDF of the paper to Project Euclid.  
- Paper is now available via Project Euclid and the GitHub Pages site.
