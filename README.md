# Tutorial Advanced Git and Git Hub Concepts
----

### Description:
* Created by: Akash Tyagi
* Date: 19-Dec-2020
* Reach me out: akashdktyagi@gmail.com
---

#### Tutorial:

* This repo is to demonstrate advanced git concepts mentioned below:
    * PR Creation (UI)
    * PR Merging (UI)
    * Code Review (UI)
    * Conflict resolution (UI/Local)
    * Revert the PR Changes (UI)
    * Practice and steps a developer has to take to complete his code work.
* I am making all the changes using Git Hub UI for the sake of simplicity.
* However, in real world this is not the usual practice.
* All the code changes happen on the local machine and developer then commits these code using git command line tool like git bash.
* Below things however happen from GitHub UI:
    * PR creation happens in UI.
    * PR review and Code Review happens in UI.
    * Revert and Roll back of PR Changes happens in UI.
* <b>Conflict Resolution:</b>
    * If conflicts are simple enough then it can be done from UI.
    * If conflicts are appearing in many files or conflict related to "Deletion" of the file.
    * For example, one developer has made a change in the file and other developer has deleted the file in his branch. 
    * In such cases it is not possible to resolve conflict from UI.
    * It is advisable to solve them in local system and use git command line to commit the changes.
* <b>Merging</b>
    * There are many other use cases as well. For example, if one developer is working on his own branch, but wishes to keep taking latest from ```master``` branch for any new updates.
    * In such cases the developer have to merge the ```master``` branch code regularly.
    * Developer can use git hub command line tool to continuously take ```master``` code in to his branch. How?
        * Navigate to your branch in local: ```git checkout my-branch```
        * Run command: ```git pull origin master``` 
        * Above command is short cut command which does "pull from master and merge it in the current branch"
        * There are other commands as well to do merging. More on this in my git command line tutorial.
* <b>In the real World these are the steps a developer has to take to finish his work.</b>

    * Each developer is assigned a ticket/jira.
    * Developer will create the branch from ```master``` (always create the branch from base branch). In some projects base branch is not master but called as ```develop``` or ```stage```
    * Developer will give a sensible name to the branch. Example: ```jira-2345-adding-search-test-cases```. where ```2345``` is the jira task/story id.
    * IMPORTANT!: No other developer is suppose to be working on that branch. One branch represents, one developer and one ticket/jira id's work only.
    * If new work, then create new task and each task will have a branch.
    * In a nutshell: JIRA ID ==> 1 Branch ==> One Developer (If this rule is broken, whole hell could break loose :-) )
    * Developer will finish his work in his branch, but before creating a Pull Request, code merge with the base branch is required. Why it is to be done?
        * There are cases where developer has to continuously take the latest code.
        * For example, he is taking 5-6 days to complete his work in his branch. Its better to check who is merging what in master branch. May be something usefull which you can use for your work.
        * Also, its a good practice to keep taking latest code from ```master``` branch in to your branch.
        * So, before creating the Pull Request, you should always merge ```master``` branch in to your local branch.
    * Developer will create the Pull Request from UI. This can not be done from Command Line.
        * As mentioned above, developer has to  merge ```master``` code in his branch before creating the PR.
        * This is to be done to check if there are any conflicts.
        * When you run git command: ```git pull origin master``` in your branch, git will not only merge the changes but it will also highlight any conflicts.
        * After conflicts are resolved developer has to run git add, git commit and git push command. This will update his branch with the conflict free master's code.
        * And then PR is to be raised.
        * <b>Please Note: If merging is not done locally. Then also, PR can be created and these conflicts can be resolved from UI. This is explained in below screenshots.</b>
    * Developer will assign reviewers.
    * Reviewers will do code review and will give comments, check the screen shots below.
    * Developer will check the review comments and make the necessary changes in the same branch and commit the changes.
    * After the changes in the same branch, same PR will automatically gets updated. No need to create new PR.
    * Once code review is successfull, reviewer will    ```approve``` the PR, i.e. PR is ready to be merged.
    * If there are any conficts with the base branch, then those conflicts has to be resolved before PR can be merged.
    * How to do conflict resolution is explained in above lines as well in below screen shots.
    * Once every thing is ok i.e. no conflict, necessary code review and approval is given and in some cases Sonar Qube is also executed; Then code is finally merged.
    * In case, code changes are to be reverted, then Open the merged PR and click on Revert. The steps to this are explained at the bottom of this tutorial.
    
---
## Steps to be taken
* Below screen shots explain there possible cases when two developers are working on the repository.
* You can follow screen shot step by step to practice these 4 cases.
* Assume There are two developers working on this repo: Akash and Sarang
* Four cases are:
    * Case 1 - No Conflict
        * Akash changes Test File 1
    * Case 2 - No Conflict
        * Akash Changes Test File 1 and 
        * Sarang Changes Test File 2
    * Case 3 - Conflict will Occur
        * Akash Changes Test File 1 and same lines
        * Sarang Changes Test File 1 ans Same lines

---

### There can be these three possible cases
* Only in the last case conflict can appear.
>![Image](Screenshot%202020-12-19%20at%201.08.21%20AM.png)

## Case 1: Both developer working in different files.
>![Image](Screenshot%202020-12-19%20at%2012.36.11%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.37.01%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.37.13%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.38.03%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.38.36%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.39.15%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.39.37%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.40.02%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.40.46%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.41.03%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.42.30%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.42.41%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.42.58%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.43.09%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.43.18%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.43.27%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.43.56%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.44.31%20AM.png)

# Case 2: Two developers making changes in Different Files
>![Image](Screenshot%202020-12-19%20at%2012.53.54%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.56.28%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.56.44%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.57.21%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.57.48%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.58.16%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.58.29%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.58.52%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.59.07%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.59.20%20AM.png)

>![Image](Screenshot%202020-12-19%20at%2012.59.40%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.00.10%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.00.22%20AM.png)

# Case 3: Two developers making changes in the same file in their own respective branches
* This is where conflicts arises.
>![Image](Screenshot%202020-12-19%20at%201.08.21%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.08.00%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.19.55%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.23.17%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.23.25%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.24.12%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.24.21%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.24.49%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.25.03%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.25.14%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.25.35%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.25.48%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.25.58%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.26.20%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.27.00%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.28.44%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.29.03%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.29.14%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.29.28%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.30.02%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.30.36%20AM.png)

# How to Revert the Pull Request.

>![Image](Screenshot%202020-12-19%20at%201.31.24%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.33.33%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.33.50%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.34.18%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.34.45%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.35.02%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.35.15%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.35.32%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.35.51%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.35.55%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.36.07%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.36.18%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.36.27%20AM.png)

>![Image](Screenshot%202020-12-19%20at%201.36.46%20AM.png)


    


    
    
    
    