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
     1. On the GitHub repository page, click on the "Pull Requests" tab and click the "New Pull Request" button.
     2. Leave `base:master`; change `compare:master` to point to your branch created in step 3.
     3. The page immediatly shows the changes between your branch and master. Create the pull request by clicking the "Create Pull Request" button.
     4. Link the pull request to the issue
     5. Describe the original issue, how you fixed it and how to test your code: what pages to look at, etc.
   - Request all team members review the pull request
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
    - Keep in mind, you do not need to create a new pull request after addressing concerns. The pull request will automatically update as you make changes to the branch created in step 3. That is why you are doing this work in a issue-specific branch.
  - If yes, then move onto step 8
8. Close the issue
   - Done by lead Reviewer (Once all issues/suggestions are addressed)
   - Lead Reviewer is (1) Lacey or (2) the person who did the review if Lacey is gone.
   - Pull request is merged into the master branch
     1. Click "Conversation" tab at the top of the pull request
     2. Scroll down, click "Merge pull request" assuming there are no conflicts with the base branch. If there are conflicts then those should be fixed by the person who submitted the pull request.
     3. After you will see "Pull request successfully merged and closed" with a "Delete Branch" button. Click "Delete Branch".
   - Issue is closed
     1. The issue should be referenced in the original description of the pull request -go to it.
     2. Click "Close Issue".
   - New issue is created to update module on KnowPulse
     1. Go to https://github.com/UofS-Pulse-Binfo/KnowPulse
     2. Create an issue specifing that module XXX has received either new features or bug fixes and needs to be updated. Reference the issue linked to the pull request by entering [organization]/[repo]#[issue number] (e.g. UofS-Pulse-Binfo/tripal_daemon#3)
     3. Assign this issue to whomever is in charge of updating KnowPulse (e.g. Lacey).

## Review
- When reviewing, look at the code changes directly _and_ test through the interface.
  1. To see all the changes, click on "Files Changed" at the top of the pull request.
  2. To start a code review, hover in front of the first line you would like to comment on then click the blue + icon that shows up. This opens a comment box where you can enter your suggestion/critique. Then click the green "Start review" button.
  3. Continue adding comments throughout the changes in this manner.
- If you don't actually have code review comments to make, you can submit your review by:
  1. Click on "Files Changed" at the top of the pull request.
  2. Click on "Review Changes" button at the top right of the page.
  3. In the resulting popup, enter your comments and select whether you approve or request changes. 
- If you simply need clarification, just comment on the pull request with your questions and hold off reviewing.
- For interface functionality or design critique/suggestions, enter a comment (preferrably with screenshot) in the "Conversation" tab of the pull request.
- You may need to checkout the branch on a development site to adequetaly test the code. 
  1. `git fetch origin` will fetch all branches from that repository
  2. `git checkout -b [branch] origin/[branch]` will pull the code from the branch which you want to test
  3. Once you've finished testing, you can revert to the master branch with `git checkout master`
