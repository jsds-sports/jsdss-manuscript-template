---
title: "JSDSS instructions for reviewers"
---

This is the reviewer view of the review process. The full process is in [process.md](process.md).

## Initial review (OJS)

- Read the PDF and submit your feedback in writing in OJS.
- Wait for the AE to combine the reviews and recommend **Reject**, **Revise and resubmit**, or **Invite to GitHub Review Process**, and for the Editor to decide.

If the decision is **Reject**, you are done. If it is **Revise and resubmit**, wait for the AE to ask you to read a later PDF, if they do.

An invitation to GitHub review is **not** a conditional acceptance.

## GitHub review

If the paper is invited to GitHub review:

- Wait for the AE to create GitHub Issues from the OJS comments, create the `R0` release, and invite you as a collaborator with **Write** permissions.
- Accept the collaborator invitation.
- You may send simple, non-controversial minor edits (typos and the like) as a pull request from a branch such as `reviewer1-minor-edits` to `main`. Assign the author as **Assignee** and request the author's review. Do not merge; only the AE merges.
- Wait for the author to respond to Issues and to open one pull request per Issue on the journal repo.
- Wait for the AE to add you as a **Reviewer** on the pull requests that match your comments. You should be a GitHub Reviewer, not an Assignee (Assignees are the authors).
- Review those pull requests and approve when the Issue is addressed.
- If the author pushes a commit after you approve, that approval is stale. Review the new commits and approve again.
- Wait for the AE to confirm that every assigned Reviewer has approved, that GitHub Actions succeeded, and to merge. Only AEs merge. If the AE is not yet satisfied, review and/or revision may repeat.
- Wait for the AE to create an `R1` release after all pull requests are merged.

## Decision

- Wait for the AE to recommend **Reject** (the paper has fatal flaws that prevent publication in *JSDSS*, and authors do not want to fix them) or **Accept** (all issues have been addressed by the authors; the paper is ready for publication), and for the Editor to decide.
