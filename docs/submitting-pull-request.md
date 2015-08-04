**[⬅ Back to Coding Culture](../README.md)**

# Pull Requests

Doing does not permit code to be merged into the master branch unless it has been submitted as a Pull Request.

All Pull Requests must be reviewed by one of your peers before it can be merged into master.

#### Creating a Pull Request Assumes:

1. You have read and understand Doing's [Coding Culture](../README.md)
2. You are working off a git branch named after a corresponding Sprintly ticket
3. You have merged in the latest master branch and resolved all merge conflicts

#### Create Pull Request:

1. Commit and push your Sprintly ticket branch using [Smart Commit messages](git-best-practices.md#smart-commit-messages)
2. Visit your project's repo on [Github](https://github.com/doinginc) and click **Compare & pull request**
3. Add a Title that briefly explains the PR
4. Use the text from our [Pull Request Template](../templates/pr-template.md) as the base of your PR comment
5. Update the PR comment to complete as much information as you can provide
6. Add a Label of **Ready for Code Review**
7. Click **Create pull request**
8. One your new PR, click the checkbox under PR Author to indicate you have completed that task
9. Use HipChat to notify your peers that you have a PR that needs review
10. Watch for PR notifications and address any concerns raised by your peers

#### Review Pull Request:

1. Visit the PR you are being asked to review
2. Before starting your PR Review, remove the Label **Ready for Review** and add the Label **In Code Review**
3. Review the **Files changed** tab and add any inline comments ( click line number ) you have feedback with
4. Add any overall feedback as a new comment on the main **Conversation** tab
5. Once code review is complete, check off the items in the **PR Reviewer** once you have completed them
6. If the PR fails, remove the Label **In Code Review** and select a new label showing what action is needed
7. If the PR Passes, remove all Labels and click **Merge pull request**
8. If you are 100% certain you will never need that branch again, you can delete the branch after merging into master
9. Contact the PR Author and let them know the results of your review
10. Stay on top of any PR's you are reviewing until they are able to be successfully merged into master
