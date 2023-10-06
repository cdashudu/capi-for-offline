# Contributing to Meta CAPI for Offline :handshake:

We would love for you to contribute to Meta CAPI for Offline and help make it even better than it is
today! As a contributor, here are the guidelines we would like you to follow:

 - [Code of Conduct](#coc)
 - [Bug Report](#issue)
 - [Documentation](#doc)
 - [Submission Guidelines](#submit)
 - [Commit Message Guidelines](#commit)
 - [Contributions Under Repository License](#cla) 

## <a name="coc"></a> Code of Conduct
Help us keep Meta CAPI for Offline open and inclusive. Please read and follow our [Code of Conduct](#coc-details).


## <a name="issue"></a> Found a Bug? :beetle:
If you find a bug in the source code, you can help us by
[submitting an issue](#submit-issue) to our GitHub Repository. Even better, you can
[submit a Pull Request](#submit-pr) with a fix.

## <a name="doc"></a> Have any suggestions for the Documentation? :bulb:
If you find any discrepancies in our Documentation or you have any awesome suggestions for us, report it by opening a new issue.

### <a name="submit-pr"></a> Submitting a Pull Request (PR)
Before you submit your Pull Request (PR) consider the following guidelines:

1. Search [GitHub](https://github.com/cdashudu/capi-for-offline/pulls) for an open or closed PR
  that relates to your submission. You don't want to duplicate effort.

1. Be sure that an issue describes the problem you're fixing, or documents the design for the feature you'd like to add.
  Discussing the design up front helps to ensure that we're ready to accept your work.

1. Fork the `cdashudu/capi-for-offline` repo.

1. Make your changes in a new git branch:

     ```shell
     git checkout -b my-fix-branch main
     ```

1. Create your patch

1. Commit your changes using a descriptive commit message 

1. Push your branch to GitHub:

    ```shell
    git push origin my-fix-branch
    ```

1. In GitHub, send a pull request to `cdashudu/capi-for-offline:main`.
* If we suggest changes then:
  * Make the required updates.
  * Test if the script is running locally 
  * Rebase your branch and force push to your GitHub repository (this will update your Pull Request):

    ```shell
    git rebase master -i
    git push -f
    ```

That's it! Thank you for your contribution!

#### After your pull request is merged

After your pull request is merged, you can safely delete your branch and pull the changes
from the main (upstream) repository:

* Delete the remote branch on GitHub either through the GitHub web UI or your local shell as follows:

    ```shell
    git push origin --delete my-fix-branch
    ```

* Check out the main branch:

    ```shell
    git checkout main -f
    ```

* Delete the local branch:

    ```shell
    git branch -D my-fix-branch
    ```

* Update your master with the latest upstream version:

    ```shell
    git pull --ff upstream main
    ```

## <a name="cla"></a> Contributions Under Repository License :memo:


Whenever you make a contribution to a repository containing notice of a license, you license your contribution under the same terms, and you agree that you have the right to license your contribution under those terms. If you have a separate agreement to license your contributions under different terms, such as a contributor license agreement, that agreement will supersede.

Isn't this just how it works already? Yep. This is widely accepted as the norm in the open-source community; it's commonly referred to by the shorthand "inbound=outbound". We're just making it explicit.


## <a name="coc-details"></a> Code of Conduct :cop:

As contributors and maintainers of the Meta CAPI for Offline project, we pledge to respect everyone who contributes by posting issues, updating documentation, submitting pull requests, providing feedback in comments, and any other activities.

Communication must be constructive and never resort to personal attacks, trolling, public or private harassment, insults, or other unprofessional conduct.

We promise to extend courtesy and respect to everyone involved in this project regardless of gender, gender identity, sexual orientation, disability, age, race, ethnicity, religion, or level of experience. We expect anyone contributing to the Meta CAPI for Offline project to do the same.

If any member of the community violates this code of conduct, the maintainers of the Meta CAPI for Offline project may take action, removing issues, comments, and PRs or blocking accounts as deemed appropriate.
