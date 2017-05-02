# Developer Workflow.
This document describes the workflow that the KnowPulse team follows for development, which depends on the use of GitHub features and the [ZenHub Agile Project Management Extension for GitHub](https://www.zenhub.com/).

## All Tasks, Bugs, Features, etc. should be GitHub Issues
 - Create an issue on github: **Be Descriptive!**
 - Label the issue (bug? enhancement?)
 - Using Boards, indicate if this is a long term goal (icebox) or if you intend to do it right away (Up Next)
 - If you know who will be doing work on this issue then assign it to them.
 - Keep issues to reasonable amounts of work. A good rule of thumb is that if you think the issue would take more than a week of development time to complete, then the scope of work is not reasonable for a single issue ;-). 
 - Also keep in mind, the smaller the issue the easier it is to review and the faster it will be released.
 
## Workflow
1. Choose an issue to work on. Bugs should take priority. Look first at issues assigned to you.
2. Once you've chosen a task, assign it to yourself and move it to "In Progress" using Boards.
3. Create a local branch and push it to github _before_ making a commit. Use the format `[issue number]-[short description]` when you name the branch.
   - Create local branch: `git checkout -b [issue number]-[short description]`
   - Push it to github: `git push origin [issue number]-[short description]`
   - Any changes you will make in completing this issue should now be done within this branch.
4. Work on the issue.
   - Commit often to your local branch using descriptive commit messages.
   - Push to github at least twice a week!
   - Also, try to to keep a record of design decisions and approach to solving the issue by commenting on the issue itself. The more context that you provide, the less you will have to explain to your co-workers during review ;-)
5. Once work is complete, signal a Review
   - Create a pull request between your branch and the master branch
   - Link the pull request to the issue
   - Describe how to test your code: what pages to look at, etc.
   - Assign all team members to the pull request
   - In Boards, move the issue to the "Review" pane
6. Review
   - Give your team members a day or two to look over your code
   - Answer any questions they have
   - Wait to implement suggestions until the review process is completed by everyone
   - Reviewers should indicate whether they approve your changes or not.
7. All reviewers approved your changes?
  - If no, then go back to step 4.
    - Make sure to address all concerns. 
    - If you are uncertain their approach is the best one, then **defend yours**. Ask for clarification on any suggestions if necessary.
  - If yes, then move onto step 8
8. Close the issue
   - Done by lead Reviewer (Once all issues/suggestions are addressed)
   - Pull request is merged into the master branch
   - Issue is closed
   - New issue is created to update module on KnowPulse

## Review
- When reviewing, look at the code changes directly _and_ test through the interface.
  1. To see all the changes, click on "Files Changed" at the top of the pull request.
  2. To start a code review, hover in front of the first line you would like to comment on then click the blue + icon that shows up. This opens a comment box where you can enter your suggestion/critique. Then click the green "Start review" button.
  3. Continue adding comments throughout the changes in this manner.
- For interface functionality or design critique/suggestions, enter a comment (preferrably with screenshot) in the "Conversation" tab of the pull request.
