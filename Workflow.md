# Developer Workflow.
This document described the workflow that the KnowPulse team follows for development.

## All Tasks, Bugs, Features, etc. should be GitHub Issues
 - Create an issue on github: Be Describtive
 - Label the issue (bug? enhancement?)
 - Using Boards indicate if this is a long term goal (icebox) or if you intend to do it right away (Up Next)
 - If you know who's going to work on this then assign it to them
 
## Workflow
1. Choose an issue to work on. Bugs should take priority. Look first at issues assigned to you.
2. Once you've choosen a task, assign it to yourself and move it to "In Progress" on boards.
3. Create a local branch:  `[issue number]-[short description]` and push it to github even before making a commit.
 - `git checkout -b [issue number]-[short description]`
 - `git push origin [issue number]-[short description]`
 - All changes related to completing this issue should be done within this branch.
4. Work on the issue.
 - Commit often to your local branch using descriptive commit messages.
 - Push to github at least twice a week
 - Also, it's helpful to keep a record of design decisions and approach in the issue. Remember, the more information you put in the issue the less you will have to explain to your co-workers during review ;-)
5. Once work is complete, signal a Review
 - Create a pull request between your branch and the master branch
 - Link to the issue
 - Describe how to test: what pages to look at, etc.
 - Assign all team members to the pull request
 - Boards: Move to "Review"
6. Review
 - Give your team members a day or two to look over your code
 - Answer any questions they have
 - Wait to implement suggestions until review is complete
 - Reviewers should indicate whether they approve your changes or not.
7. All reviewers approved your changes?
- If no, then go back to step 4.
  - Make sure to address all concerns. 
  - If you are uncertain their approach is the best one then defend yours. Feel free to ask for clarification.
- If yes, then see step 8
8. Close
 - Done by lead Reviewer (Once all issues/suggestions are addressed)
 - Pull request is merged
 - Issue is closed
 - New issue is created to update module on KnowPulse
