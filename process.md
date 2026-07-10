# JSDSS Author Submission and Review Process

## 1. Author Submission

Step 1 is the recommended workflow and submission process for authors. 

Alternatively, authors can choose to submit a PDF created in another manner to the OJS system (ZZZ link). However, note that using this template will eventually be required before publication if your manuscript proceeds along the review process and into the GitHub review stage (see step 2+). 

- Create a new repo in **your** GitHub account using the template repository: [`jsds-sports/jsdss-manuscript-template`](https://github.com/jsds-sports/jsdss-manuscript-template).
    - Go to: <https://github.com/jsds-sports/jsdss-manuscript-template>
    - Click **Use This Template** in the upper right.
    - Toggle **Include All Branches** on.
    - Give the repo a reasonable name of your choice.
    - You may choose to change the visibility to **Private** while working on the project.
    - Click **Create Repo**.
- Clone repo to your machine.
- Write paper with code and data. Use the Quarto template for the paper.
- Submit PDF to the OJS system at Charlotte (ZZZ link)
- ZZZ Author submits URL for repo, or adds editor as a collaborator to repo

## 2. *JSDSS* Review Process

- An editor and multiple reviewers read the PDF.
- If there is sufficient interest in potentially publishing the paper, we invite the author to submit for a GitHub review. 

(ZZZ the rest of the section below is for the GitHub review process. Much of it doesn't involve the Author. We should have another (simpler) set of instructions only for the authors. Also, the GitHub Actions pass probably needs to move to later, based on our discussions on 7/10/2026.)

    - The author is responsible for putting the paper contents in our Quarto format (as laid out in the template repo). (ZZZ add pro tips, like `pandoc` code. We should try this first.)
    - The GitHub Actions script that is already part of the template needs to execute correctly. This will be executed automatically when the author pushes changes to the repo on GitHub.
- Upon successful rendering via GitHub Actions in the **author's** repo, the reproducibility editor **forks** the author's repo into the `jsds-sports` GitHub Organization.
    - At this point, the author should create a [**release**](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases) at the time the repo is forked.
    - After it is forked, the author also makes the repo public (perhaps temporarily), to give the Editors Change Visibility permissions when the article is ready to be published. The Editors won't change Private to Public until final publication. 
    - If the author doesn't want the repo to be public yet, they can immediately Change Visibility to Private again. Otherwise, the author can leave it as Public.
    - *JSDSS* editor goes to Settings page
        - General
            - Check that Change Visibility permissions are available. Otherwise, ask author to do the previous step.
            - Rename the repo to match the OJS paper ID tracking system (e.g., `2026-baumer-413`).
            - Enable Issues 
        - Rules, rulesets
            - Create Protect Main Branch rule (ZZZ can we create a org-wide template?)
                - New branch ruleset
                - Default branch (main)
                - Click Require a pull request before merging
        - Pages
            - In the branch section, chooses `gh-pages`. 
        - Actions
            - Select **Quarto Publish** on the left, and select **Run Workflow** on the right to confirm GitHub Actions has no problems. (It Auto ran when it was public, but does not auto run when it's private.)
        - Collaborators and Teams
            -  Invite Authors as collaborators with direct access and **Write** permissions 
    - Editor goes to main repo page and creates an `R0` release in the forked repo.

## 3. *JSDSS* GitHub Review Process

- (ZZZ this should change based on our discussion today. We can start the review process in GitHub without doing reproducibility checks.) The GitHub Actions script that is already part of the template needs to execute correctly.
    - If that works, the paper data and code go to the reproducibility editor for review.
- **Main comments:** Editor collates comments from reviewers posted in OJS and creates [GitHub Issues](https://docs.github.com/en/issues/tracking-your-work-with-issues/learning-about-issues/about-issues) for more substantive feedback.
    - One Issue per main comment (could be from multiple reviewers).
    - One Issue for all typos and minor suggestions.
    - Editor assigns Issue to the author, reviewer(s) that gave feedback related to that Issue, and themselves.
- **Minor edits:** At any time throughout this process, the reproducibility editor (and other reviewers) can send simple, non-controversial minor edits back to the author via a pull request from `jsds-sports/2026.baumer.736 reviewer1-edits` to `jsds-sports/2026.baumer.736 main` (using the suggestions feature) and adding the author as the reviewer.

## 4. Revision Phase

- Author will respond to GitHub Issues (can ask clarifications, push back, etc.) by commenting via the web interface.
- Author edits the original repo on their account.
    - Commits should be tagged to Issues.
- For each Issue, the author
    - Creates a new branch on the JSDSS repo `jsds-sports/2026-baumer-413` to address that Issue, and makes edits on that branch.
    - Creates a pull request from the branch to `jsds-sports/2026-baumer-413 main` and can send commits to this branch as they see fit (may need to **Change Base**)
    - Ensures that all feedback from the Issue are addressed in the pull request.    
    - Tags the Editor to review the pull request. ZZZ Should they tag the reviewers that are named on the Issue?
- The author repeats for each Issue. If there are 5 Issues there will be 5 brances and 5 pull requests. 
    - (ZZZ maybe move down? See first comment in #3) If the GitHub Actions script works, the Editor merges the pull request and creates an `R1` release.

## 5. Repeat Steps 3 and 4

- Repeat the reproducibility review and revision phases until the Editor is satisfied.

## 6. Production Phase

- Author signs copyright forms.
- Editor obtains a DOI for the paper.
- Editor adds watermark and logo to the paper for authenticity.
- Editor creates a `final` release and the repo is frozen.
- GitHub Pages is turned **ON** and the paper is available in HTML/PDF/Word formats at `https://jsds-sports.github.io/2026-baumer-413/`.
- Editor adds that URL and paper metadata to the `jsds-sports.github.io` main website.
- Editor adds PDF of the paper to Project Euclid.  
- Paper is now available via Project Euclid and the GitHub Pages site.
- ZZZ may need to include something about checking OJS and availability on OJS