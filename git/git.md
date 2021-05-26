# <span class="header">Introduction to Git</span>

So, Firstly What is Git ? <span class="highlight">Git is one of the most popular Version Control System.</span>

>A Version Control System records the changes made to our code over-time and stores it in a special database called repository.

We can often look at our project history and see who has made what changes , when & why. One of the biggest advantage of Git is that if we do something wrong we can easily revert our project back to earlier state. Now before we go further, we need to know what category of version control git falls into as this will help us understand the advantages of Git in more detail.

There are basically two types of version control system :

<center>

| Centralized | Distributed |
| :---------: | :---------: |
| In a Centralized System , all members connect to a central server to get the latest copy of the code and to share changes with others | In a Distributed System, every member has a copy of the project with its history on the machine so we can save our project locally on our machine |
| eg : Subversion , Microsoft team foundation server | eg : Git , Mercurial | 
| Problem with Centralized System is the single point failure, if the server goes offline we cannot collaborate our project so we have to wait until server is back online | In Distributed System such kind of failure cant occur since ever member has a copy of the project on his/her local machine and if the server is offline we can synchronize our work directly with each other |

</center>

<center><i>Types of Version Control System</i></center>

<br>

## <span class="header2">Why use Git ?</span>

* Free
* Open Source
* Super Fast
* Scalable
* Cheap Branching/Merging

## <span class="header2">How to use Git </span>

As Coders whose daily work revolves around working with a team on a single project, making sure everyone and everything is on the same level is quite important for a smooth performance of the team. This makes learning Git very very essential.

Before we get into the intricate details of how Git actually works, we must go through some essential commands that every git user must know. Most of these commands are what we will be using in our day-to-day activities.

### <span class="header3">Git Commands</span> 

<center>

<table>
<tr>
<th>Stages</th>
<th>Commands</th>
<th>Function</th>
</tr>
<tr>
<td>Setup</td>
<td>git config</td>
<td>Used to configure values on global or local project</td>
</tr>
<tr>
<td rowspan="4">Staging & Commit</td>
<td>git init</td>
<td>Creates an empty local repository</td>
</tr>
<tr>
<td>git add</td>
<td>Adds files to the staging area </td>
</tr>
<tr>
<td>git commit</td>
<td>Records the changes made to the code and saves it in the local repository with a meaning</td>
</tr>
<tr>
<td>git clone</td>
<td>Used to make a copy of the specified repository</td>
</tr>
<tr>
<td rowspan="4">Inspecting</td>
<td>git log</td>
<td> Used to display the commits history and status of head</td>
</tr>
<tr>
<td>git diff</td>
<td>Used to show changes between commits, working tree, etc</td>
</tr>
<tr>
<td>git status</td>
<td>Used to display the state of repository and staging area</td>
</tr>
<tr>
<td>git show</td>
<td>Used to show modifications in the commits</td>
</tr>
<tr>
<td rowspan="3">Branching & Merging</td>
<td>git branch</td>
<td>It allows us to create, list, rename and delete branches</td>
<tr>
<td>git merge</td>
<td>It is used to merge branches that have a common base commit</td>
</tr>
<tr>
<td>git checkout</td>
<td>Allows us to switch to a specific branch, create a new branch, checkout a remote branch, etc</td>
</tr>
<tr>
<td rowspan="3">Undoing changes</td>
<td>git revert</td>
<td>Creates a new commit with the previous commit that you are reverting back to but unlike reset where it removes any other commits on its way back, instead it simply makes a copy of that and moves forward </td>
</tr>
<tr>
<td>git reset</td>
<td>Allows you to go back to a previous commit and removes any other commits on its way back</td>
</tr>
<tr>
<td>git rm</td>
<td>Used to remove files from the working tree and index</td>
</tr>
<tr>
<td rowspan="3">Collaborating changes</td>
<td>git fetch</td>
<td>It downloads new data from remote repository but doesn't integrate any of these new changes into our working files</td>
</tr>
<tr>
<td>git pull</td>
<td>It downloads new data from remote repository and also integrates all of these new changes into our working files</td>
</tr>
<tr>
<td>git push</td>
<td>It uploads and commits the content from the local repository to the remote repository</td>
</tr>
</table>

</center>

## <span class="header2">Git Workflow for developers</span>

Understanding the workflow of git is essential, as it will help us in being efficient and correcting if any errors are caused.

<center>
<img src="../assests/GitWorkflow.jpg" width="800">
</center>

The Workflow goes something like :-
1. Clone the project from remote repository.
2. Whenever we need to save new files, we need to add the files first to staging area
3. Only after files are added to staging area, we can commit them into our local repository.
4. We can use commit -a as a shortcut to directly commit in local repository.(If new files were created, do not use this.)
5. Later on, we can push our local repository code to remote repository when we have reached some kind of milestone.
6. Command fetch can be used to retrieve latest data from remote repository.
7. Using merge we can add the newly retrieved data into our working directory(Must be used careful or else will show conflict)
8. git pull is shortcut to straight away add latest data from remote repository.(Must be used when we are 100% sure as it will commit the changes)
9. git diff head and diff are used to check difference between working directory and staging area or local repository


## <span class="header2">Git Workflow for application</span>
 
<center>
<img src="../assests/GitDevWorkflow.jpg" width="800">
</center>

* New development and non emergency are built in feature branches
* Feature branches are branched off of the develop branch, and finished features and fixes are merged back into the develop branch.
* When it is time to make a release, a release branch is created off of develop
* The code in the release branch is deployed onto a suitable test environment, tested, and any problems are fixed directly in the release branch. 
* The master branch tracks released code only. The only commits to master are merges from release branches and hotfix branches.
* Hotfix branches are used to create emergency fixes.

<style>
.highlight{
  color: #75FF33
}
.list{
  color: #FF8080
}
.header3{
  color: #E6D100
}
.header{
  color: #EE82EE
}
.header2{
  color: #00FFFF
}
</style>
