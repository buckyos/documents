![CYFS logo](https://github.com/buckyos/CYFS/blob/main/doc/logos/CYFS_logo.png)

-   We will collect knowledges about `CYFS` here.
-   Anyone can submit their insights or introductory documents, it may be employed in the official documentation repository.
-   You can learn here when you have some problems.
-   You can make an issue or discussion when you cannot fix your problem yourself or you found an error.

# How to manage the documents?

-   There are 3 branchs in the [repository](https://github.com/buckyos/documents):

| Branch   | Description                        | Inclusion conditions                                                                                                                                          | Manager                                                         |
| -------- | ---------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| official | Documents approved by the team     | Accurate content, high level of writing, easy to understand                                                                                                   | Senior developers of relevant modules + project administrators  |
| checked  | Documentation reviewed by the team | The content is accurate, but the writing is flawed and difficult to read                                                                                      | Senior developers of relevant modules or project administrators |
| draft    | Unchecked document                 | There may be errors in the content, which need to be corrected. If you find an error, you can initiate a discussion or submit a `Pull request` to correct it. | Any one can update the repository                               |

1. When you want to submit a document, you should do as follow:

    - Fork the branch `draft` to your own repository.
    - Finish your documents, create a new one or update an exist one.
    - Post a `Pull request` to the branch `draft` in official repository.
    - Wait the team to merge your documents, you can also create a issue or discussion to publish your documents.

2. When someone with `write` permissions find a `Pull request`, he can do as follow:

    - If obvious problems are found, reject it and note the reason.
    - Otherwise merge it to the branch `draft`.

3. The managers periodically compares `draft` and `checked` branches, They will check the `Commit`s as follow:

    - Make a `Patch` include the proofreaded `Commit`s in the `draft` branch.
    - Ignore the `Commit`s with errors and feedback to the writer(create a discussion and @ the auther?).

4. How to decide to include the `Patch`?

    - Issue a vote on `Patch`, the lead developers of related modules and managers are invited to join.
    - They will give each commit a score while voting.
    - If the vote is passed, the `Patch` will be included in the `checked` branch, otherwise the error in it will be noted.
    - If the score is high enough, the `Patch` will be included in the `official` branch.

        **Notes: We use `cherry-pick` or `format-patch` to merge each commit, instead of `merge` or `rebase`, to avoid merging unqualified commits into. Therefore, we should submit as little and complete content as possible each time.**

    ```
    git cherry-pick <commit-hash>
    git format-path ...
    ```
