# Open Source
---
This repo will be a markdown of information on contributing to open source projects.

# Benefits of contributing to open source projects
---
#### Helps you improve your coding techniques

    When coding with others on a project, you are forced to reevaluate the best way to 
    implement your code. When someone reviews your pull request, they will give helpful 
    criticism which you can learn from and take with you as you continue to contribute to 
    technical projects.

#### Opportunity to work on your communication

    To work with others, you communicate your reasoning for how and why you implemented your 
    code the way you did.

#### Increase visibility in the community

    When contributing to open source projects, you allow others to view your work and 
    continued effort to the community which helps your standing in the community but 
    also how future prosepective employers might view you as you move along.
    
#### And the obvious...

    Help improve peoples programs!

# How to find open source projects
---

First, we must be able to find these open source projects. There are two different 
ways (that I've found) to find these open source projects.

1. Search in the github search bar using a qualifier
- Go to [Github](https://www.github.com)
- In the search bar...
    - Enter in the qualifier in the form -> [label-you-are-searching-for]:>n
    - **good-first-issues:>2 javascript** here we see a label of "good-first-issues", 
    a repo containing more than 2 issues, and contains the keyword "javascript"

 2. Go to a number of websites which have found the repos and aggregated them into lists
 based on labels or issues. A list of websites I've found are...
- [First Timers Only](https://www.firsttimersonly.com/)

- [Code Triage](https://www.codetriage.com/)

- [Github repo of big open source projects by language](https://github.com/MunGell/awesome-for-beginners)

- [Open Hatch](https://openhatch.org/search/?q=&language=JavaScript)

- [Open Source Fridays by Github](https://opensourcefriday.com/)

- [Contrib](https://gauger.io/contrib/#/language/javascript)

- [Fixme](https://fixme.ossn.club/)

- [ContributorNinja: Organized by language](https://contributor.ninja/)

- [Up For Grabs](https://up-for-grabs.net/#/)

Soo many links... There are more than this but this, plus the github search/explore options provide endless 
ways to find the right open source project for you!
    
    
# Git workflow to contribute to open source projects
---

1. Fork the repository
- go to the repo and usually in the top right there is a "fork" option
- it should fork a repo into the account you are signed in on
2. Clone the repo using the project url or ssh option on the repo
```
git clone git@github.com:yourgithubuser/project.git
```
3. Set original project as upstream (note: this will not make the original project origin, origin is still on your forked repo)
```
git remote add upstream git@github.com:entity/project.git
```

**The next steps will repeated as you work with your forked project**
4. Before working on changes, make sure that the master/default branch of your forked repo is synchronized
with the master/default branch of the original project repo.
```
git checkout master
git fetch upstream
git merge upstream/master
git push origin master
```
5. Name a new branch and switch to it (name it after the bug fix, the feature added, tracker issue, or documentation update), make sure
that the branch does not exist already.
```
git branch
git checkout -b myfixes
```
the first command lists local branches that exist, and then the second creates and checks out the new branch named "myfixes"
6. After working on the changes, commit them.
```
git commit -a -m "My fixes"
```
**Note:** the a flag stages the untracked files just like `git add -u` unlike `git add .` which includes untracked files as long as they
contain modifications. With this command given, git add will not be necessary.
7. Changes might have occurred while you were working on the project, so to get a fast forward merge, use the following git commands to
rebase your branch.
```
git checkout myfixes
git pull --rebase upstream master
```
**Note:** There may be conflicts, but this is normal especially working on active open source projects.
8. After resolving the merge conflicts, go to your forked repo on your github profile. Then click on "Pull Request". Make sure you choose upstream repo "master" as the destination branch and your forked repo "myfixes" as the source branch (the branch will be automatically removed for you after the pull request is accepted)

    
