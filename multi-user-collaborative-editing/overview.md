# Overview

## Benefits of Using GitHub

Vivliostyle Pub uses an external version control system, [GitHub](https://github.co.jp/), to manage user files. For users, version control systems offer the following benefits:

1. Record file change history
2. Revert files to previous states
3. Enable collaborative editing by multiple users

Unfortunately, the current version of Vivliostyle Pub does not support the above features 1 and 2. These features can be used with various GitHub clients. There are various free clients available, such as [Sourcetree](https://www.sourcetreeapp.com/). For example, refer to the following for operations using the official GitHub client, [GitHub Desktop](https://docs.github.com/desktop/installing-and-configuring-github-desktop) (free).

- [Viewing the branch history](https://docs.github.com/desktop/contributing-and-collaborating-using-github-desktop/making-changes-in-a-branch/viewing-the-branch-history)
- [Committing and reviewing changes to your project](https://docs.github.com/desktop/contributing-and-collaborating-using-github-desktop/making-changes-in-a-branch/committing-and-reviewing-changes-to-your-project)

Here, we will explain how to perform collaborative editing by multiple users using Vivliostyle Pub.

## Overview of Collaborative Editing

(In this document, individual workers are referred to as "committers" and those who oversee the project are referred to as "administrators")

In collaborative editing, we use GitHub's [Protected Branches](https://docs.github.com/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/about-protected-branches) feature. This feature prohibits direct editing in the default branch, which is the main branch, and enforces that workers edit in their own working branches, which are merged into the default branch through administrator reviews. As a result of such collaborative work, documents with fewer errors can be efficiently produced.

Collaborative editing generally proceeds as follows (explained in the following sections).

1. [Committer creates a new branch in the GitHub repository](/multi-user-collaborative-editing/working-procedure-first-part.md#committer-creates-a-new-branch-in-the-github-repository)
1. [Committer selects the branch in Vivliostyle Pub](/multi-user-collaborative-editing/working-procedure-first-part.md#committer-selects-the-branch-in-vivliostyle-pub)
1. [Committer edits and saves the document in Vivliostyle Pub](/multi-user-collaborative-editing/working-procedure-first-part.md#committer-edits-saves-the-document-in-vivliostyle-pub)
1. [Committer creates a pull request on GitHub](/multi-user-collaborative-editing/working-procedure-latter-part.md#committer-creates-a-pull-request-on-github)
1. [Administrator reviews, approves, and merges the pull request on GitHub](/multi-user-collaborative-editing/working-procedure-latter-part.md#administrator-reviews-approves-and-merges-the-pull-request-on-github)

## Conditions Required for Collaborative Editing

To use the [Protected Branches](https://docs.github.com/repositories/configuring-branches-and-merges-in-your-repository/defining-the-mergeability-of-pull-requests/about-protected-branches) feature mentioned above in your repository, you need to obtain a paid GitHub account or make the repository public if you have a free account. For details, refer to the following.

- [Overview of GitHub's products and pricing plans](https://docs.github.com/get-started/learning-about-github/githubs-products)

However, even with a free account, you can participate in collaborative editing if you are invited to the repository by an eligible person. Refer to the following.

- **Reference:** [Inviting collaborators to a personal repository](https://docs.github.com/account-and-profile/setting-up-and-managing-your-github-user-account/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository)