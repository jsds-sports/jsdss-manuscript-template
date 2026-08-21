---
title: "JSDSS instructions for associate editors"
---

This is the Associate Editor (AE) view of the review process. The full process is in [process.md](process.md).

## Initial review

- Wait for the Editor to decide the paper is appropriate for *JSDSS* and to assign it to you.
- Read the paper and decide whether it merits a full review.
    - If not, recommend **Reject** without further review.
    - If it does, assign **at least two** peer reviewers to read the PDF and submit written feedback.
- Wait for the reviewers to submit their feedback in writing.
- Combine the reviewers' feedback with your own and make *exactly one* recommendation:
    - **Reject**: no viable path to publication.
    - **Revise and resubmit**: a path exists, but substantive problems must be fixed before GitHub review.
    - **Invite to GitHub Review Process**: a path exists and you want a deeper review.
- Wait for the Editor to decide.

An invitation to GitHub review is **not** a conditional acceptance. **Reject** and **Invite to GitHub Review Process** are terminal initial-review decisions. **Revise and resubmit** may happen more than once. If it does, the author revises and resubmits the PDF; you may ask the reviewers to read the later PDF.

## Start GitHub review

If the Editor invites the paper and the author continues:

- Wait for the author to put the paper in *JSDSS* Quarto format in a private GitHub repo, for GitHub Actions on **their** repo to render successfully, and for the author to invite you to that repo.
- Fork the author's repo into the `jsds-sports` organization.
    - Uncheck "Copy the main branch only".
    - The journal fork must be **private** when created. Keep it private until final publication.
- Wait for the author to make **their** repo public (they may switch it back to private). That is what lets you use **Change Visibility** on the journal fork later.
- On the journal fork, open Settings:
    - General: confirm Change Visibility is available (if not, ask the author to make their repo public); rename to the OJS id (e.g. `2026-001-lastname-GHusername`); enable Issues; confirm GitHub Actions renders.
    - Collaborators and Teams: invite authors and reviewers with **Write** permissions.
- On the journal fork, create the `R0` [release](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases). Only you create `R0`. The author does not create a release on their repo.

All official Issues and pull requests happen on the journal fork.

## Review phase

- Collate OJS reviewer comments into GitHub Issues.
    - One Issue per main comment (a comment may come from more than one reviewer).
    - One Issue for all typos and minor suggestions.
    - Assign each Issue to the author, the reviewer(s) who raised it, and yourself.
- You (or a reviewer) may send simple, non-controversial minor edits as a pull request to `main`. Assign the author as **Assignee** and request the author's review. You still merge.

## Revision phase

- Wait for the author to respond on the Issues and to open one pull request per Issue on `jsds-sports/2026-001-lastname-GHusername` (edits on the journal repo, commits linked to Issues).
- After each pull request is opened, set GitHub roles:
    - **Reviewers:** the peer reviewers for that Issue (not the authors).
    - **Assignees:** the authors. Assign the lead author; they may assign a co-author.
- Wait for every Reviewer assigned to that pull request to approve. Required Approvals is set to 1; that is a floor. Check that all assigned Reviewers have approved before you merge.
- If a commit is pushed after an approval, that approval is stale. Wait for the Reviewers to approve again.
- If GitHub Actions succeeds, all assigned Reviewers have approved, and you are satisfied, merge the pull request. Only AEs merge. Otherwise, the review and/or revision phases may be repeated until you are satisfied.
- After all pull requests are merged, create an `R1` release.

## Decision

- Make *exactly one* recommendation to the Editor: **Reject** (the paper has fatal flaws that prevent publication in *JSDSS*, and authors do not want to fix them) or **Accept** (all issues have been addressed by the authors; the paper is ready for publication).
- Wait for the Editor to decide.

## Production

Keep the journal fork private until publication.

- Wait for the author to sign copyright forms.
- Wait for the Editor to obtain a DOI, add the watermark and logo, create the `final` release, turn on GitHub Pages, add the paper to `jsds-sports.github.io`, and post the PDF to Project Euclid.
- Change the journal repo from Private to Public only at final publication.
