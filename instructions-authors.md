---
title: "JSDSS instructions for authors"
---

This is the author view of the review process. The full process is in [process.md](process.md).

## Prepare and submit

- Create a new repo in **your** GitHub account from the template [`jsds-sports/jsdss-manuscript-template`](https://github.com/jsds-sports/jsdss-manuscript-template).
    - Click **Use This Template**, toggle **Include All Branches** ON, name the repo, and create it.
    - You may keep the repo **Private** while you work.
- Clone the repo, write the paper with code and data in the Quarto template, and generate a PDF.
- Include a URL for the repo in the Acknowledgement section, or add an editor as a collaborator.
- Submit the PDF to the [OJS system at Charlotte](https://journals.charlotte.edu/).

You may submit a PDF produced another way. The [Quarto template](https://github.com/jsds-sports/jsdss-manuscript-template) will be required if the paper is invited to the [GitHub review stage](process.md#sec-github).

## Initial review

- Wait for the Editor's decision, either **Reject**, **Revise and resubmit**, or **Invite to GitHub Review Process**. Then you may continue or withdraw.
- **Revise and resubmit** can happen more than once. If you continue, revise the PDF, resubmit, and wait for the Editor again.
- **Reject** and **Invite to GitHub Review Process** are terminal initial-review decisions.
- An invitation to GitHub review is **not** a conditional acceptance.

## Start GitHub review

If you are invited and choose to continue:

- Put the paper in *JSDSS* Quarto format in a GitHub repo, as in the prepare step, if you haven't already. Keep that repo private.
- Push to GitHub so that the template GitHub Actions workflow renders successfully.
- Invite the AE to your repo.
- Wait for the AE to fork your repo into the `jsds-sports` organization (the journal fork stays **private**).
- After the fork exists, make **your** repo public (you may switch it back to private immediately). This lets the AE use **Change Visibility** on the journal fork at publication.
- Wait for the AE to finish journal-fork setup: confirm Change Visibility, rename the repo (e.g. `2026-001-lastname-GHusername`), enable Issues, invite you as a collaborator with **Write**, and create the `R0` release.

From this point, do all official work on the journal fork. You may still push to your personal repo if you want.

## GitHub review and revision

- Wait for the AE to open GitHub Issues from the OJS reviewer comments (one Issue per main comment; one Issue for typos and minor suggestions).
- The AE or a reviewer may send a minor-edits pull request. You are the **Assignee** and should review those edits. Do not merge; the AE merges.
- Respond to Issues on GitHub (clarifications, push-back, and so on).
- Edit the **journal** repo, not your own. Link commits to Issues.
- For each Issue:
    - Create a branch on `jsds-sports/2026-001-lastname-GHusername` and make the edits there.
    - Open a pull request to `main` and address all feedback from that Issue.
- If there are 5 Issues, there will be 5 branches and 5 pull requests.
- After each pull request is open, wait for the AE to set **Reviewers** (the peer reviewers) and **Assignees** (you). If you are the lead author, you may then assign a co-author.
- Wait for the assigned Reviewers to approve. If you push a commit after an approval, that approval is stale; wait for the Reviewers to approve again.
- Wait for the AE to merge. Only AEs merge pull requests. If the AE is not yet satisfied, the review and/or revision steps may repeat until they are.
- Wait for the AE to create an `R1` release after all pull requests are merged.

## Decision

- Wait for the AE to recommend **Reject** (the paper has fatal flaws that prevent publication in *JSDSS*, and authors do not want to fix them) or **Accept** (all issues have been addressed by the authors; the paper is ready for publication), and for the Editor to decide.

## Production

If the paper is accepted:

- Sign the copyright forms.
- Wait for the Editor to obtain a DOI, add the watermark and logo, create the `final` release, turn on GitHub Pages, add the paper to the journal site, and post the PDF to Project Euclid.

The paper will be at `https://jsds-sports.github.io/2026-001-lastname-GHusername/` and on Project Euclid.
