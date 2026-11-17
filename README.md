1st
PART 1 – Git Setup (Do this once)
git --version
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --global --list
PART 2 – Create the Project folder
mkdir Gitlab
cd Gitlab
git init
ls -a
git status
PART 3 – Create the File
Method A: touch (create an empty file)
touch program1.txt
git status

Method B: nano (create and edit the file directly)
nano program1.txt
Type:
Student Name: Rahul
USN: 101
Branch: CSE-CY	

Save in nano: Ctrl + O → Enter
Exit nano: Ctrl + X
Note: If you use touch first, you can later run nano student.txt to edit the empty file.
 
Method C: notepad
notepad program1.txt

PART 4 – Check the New File
git status

PART 5 – Stage the File                                                                                      git restore --staged marks.py
git add program1.txt
git status
PART 6 – First Commit
git commit -m "VERSION 1"

PART 7 – View Commit History
git log
git log --oneline
git show HEAD
PART 8 – Modify the File
nano program1.txt
Add: Semester: 3
Save: Ctrl + O → Enter
Exit: Ctrl + X
PART 9 – See What Changed
git status									
git diff                        
PART 10 – Stage and Review the Change
git add program1.txt
               
PART 11 – Commit the Modification
git commit -m "VERSION 2"

PART 12 – Demonstrate git commit -am
Modify program1.txt         again using nano program1.txt
git commit -am "Update semester"




2nd
STEP 1: Navigate to the Git project folder

cd Gitlab

STEP 2: View the commit history

git log --oneline

STEP 3: Check the available branches

git branch
STEP 4: Create feature-branch

git branch feature-branch

STEP 5: Verify the newly created branch
  
git branch


PART 3 – SWITCH TO feature-branch
STEP 6: Switch to feature-branch

git checkout feature-branch



STEP 7: Verify the active branch

git branch

PART 4 – MAKE A SAMPLE CHANGE IN feature-branch
STEP 8: Check the folder contents

ls

STEP 9: Create or edit a file

nano filel.txt

Enter sample content:
Name: Student
Branch: CSE(CY)
Save and exit nano:
Ctrl + O  →  Enter
Ctrl + X

STEP 10: Check the changes

git status



STEP 11: Stage the change

git add filel.txt


STEP 12: Verify the staged change

git status

STEP 13: Commit the change

git commit -m " This file is created in feature-branch”

STEP 14: View the feature branch history

git log --oneline


PART 5 – SWITCH BACK TO THE master BRANCH
STEP 15: Switch to master

git checkout master

STEP 16: Verify the active branch

git branch

STEP 17: View master history before merging

git log –oneline

STEP 18: Check the master folder contents

ls
STEP 19: Merge feature-branch into master

git merge feature-branch

STEP 20: Check the repository status

git status

STEP 21: Verify the merged file

ls

STEP 22: View the merged history

git log --oneline



PART 7 – VERIFY THE BRANCHES
STEP 24: List all branches

git branch

STEP 25: Display branch details

git branch -v

STEP 26: Check merged branches

git branch --merged


PART 8 – DELETE feature-branch AFTER SUCCESSFUL MERGE
STEP 27: Delete the merged feature branch

git branch -d feature-branch

STEP 28: Verify branch deletion

git branch




3rd
PART 1 – OPEN THE GIT REPOSITORY AND CHECK EXISTING BRANCHES
	Navigate to the Git project folder
cd Gitlab
 
	View the commit history
git log --oneline

	Check the available branches
git branch

PART 2 – SWITCH TO THE WORKING BRANCH
	Switch to the feature branch
git checkout feature-branch

	Verify the active branch
                   git branch
PART 3 – MAKE SAMPLE CHANGES IN feature-branch
	Check the folder contents
ls

	Create or edit a file
nano student.txt
Enter sample content:
Name: Student
Branch: CSE(CY)
Activity: Git Stashing
Save and exit nano:
Ctrl + O → Enter
Ctrl + X

	Check the changes
git status

PART 4 – STASH THE CHANGES
	Stash the current changes
git stash save "My temporary changes on student.txt"

	Verify the repository status
git status
	View the available stashes
git stash list
The most recent stash will normally appear as:
stash@{0}

PART 5 – SWITCH TO ANOTHER BRANCH
	Switch to the master branch
git checkout master

	Verify the active branch
git branch

	Check the folder contents
ls

PART 6 – APPLY THE STASHED CHANGES
	View the available stashes
git stash list

	Apply the most recent stash
git add .
git stash apply

	Check the repository status
git status

	Verify the applied changes
ls

	View the contents of the file
cat student.txt
The contents that were previously stashed should now be visible.

PART 7 – VERIFY THE STASH
	View the stash list
git stash list

	Remove the stash after successful application
git stash drop

	Verify the stash list
git stash list

	Remove the all stashes
git stash clear




4th
STEP 1: Open GitHub
Open a web browser such as Chrome or Edge and visit GitHub: https://github.com/

STEP 2: Click Sign Up
Click Sign up and enter the required details such as email address, password, and username. Complete the verification steps requested by GitHub.

STEP 3: Verify Your Email
Check the registered email account and complete the email verification process sent by GitHub.


STEP 4: Sign In to GitHub
Click Sign in and enter your GitHub username/email and password.

PART 2 – CREATE A REMOTE GITHUB REPOSITORY
 Create a New Repository
After signing in, click the + button at the top-right corner and select New repository.
Enter Repository Name
Enter the repository name:

Experiment4

Add a Description(optional)
Enter the following optional description:
  
Git Experiment4: cloning

Select Repository Visibility
For classroom practice, select Public. Private may also be used if required.


 Initialize the Repository
Select the option to add a README file:

☑ Add a README file

Click Create repository.

PART 3 – COPY THE REMOTE REPOSITORY URL
 Click Code
Inside the Experiment4 repository, click the green Code button.

Select HTTPS and Copy the URL
Make sure HTTPS is selected and click Copy. The URL will look similar to:

https://github.com/YourUsername/Experiment4.git

Use your actual GitHub username. Copy the URL directly from GitHub instead of typing it manually.



PART 4 – OPEN GIT BASH
Open Git Bash
On Windows, open Start → Search → Git Bash → Open.

PART 5 – CREATE A SEPARATE FOLDER FOR EXPERIMENT 4
Do not use the Gitlab folder from Experiments 1–3. Create a separate folder so that previous experiment work is not disturbed.

 Go to Desktop

cd Desktop

Create Experiment4 Folder

mkdir Experiment4


Enter Experiment4 Folder

cd Experiment4



PART 6 – CLONE THE REMOTE REPOSITORY
Clone the GitHub Repository
Use the HTTPS URL copied from GitHub:
git clone https://github.com/YourUsername/Experiment4.git

Replace YourUsername with your actual GitHub username and press Enter.
Git will download the repository. You may see messages such as:
Cloning into 'Experiment4'...
remote: Enumerating objects...
Receiving objects...
done.

PART 7 – CHECK THE CLONED REPOSITORY
 List the Folders
ls
Expected folder:
Experiment4

 Enter the Cloned Repository

cd Experiment4


 Check Git Status

git status

Expected result may be similar to:
On branch main
nothing to commit, working tree clean

The branch may be named main or master depending on the repository.

PART 8 – CHECK THE REMOTE CONNECTION
Display the Remote Repository

git remote -v

Expected output will be similar to:

origin  https://github.com/YourUsername/Experiment4.git (fetch)
origin  https://github.com/YourUsername/Experiment4.git (push)

The name origin is the default name Git gives to the remote repository after cloning.

PART 9 – VIEW THE DOWNLOADED FILE
 List the Files

ls

Because a README file was created on GitHub, you should normally see:

README.md

Display README Contents
cat README.md




5th
PART 1 – OPEN GIT BASH AND ENTER THE REPOSITORY

⮚	Open Git Bash
Open Windows Start, search for Git Bash, and launch it.

⮚	Go to Desktop
Navigate to the Desktop folder.
cd Desktop

⮚	Enter the outer Experiment4 folder
Open the folder created during Experiment 4.
cd Experiment4

⮚	Enter the cloned repository
Open the repository cloned inside the outer folder.
cd Experiment4



⮚	Verify the repository folder
Display the current path and hidden files.
pwd
ls -a

Expected result: You should see the .git directory and README.md.
PART 2 – CHECK THE CURRENT BRANCH AND REMOTE

⮚	Check the current branch
git branch

⮚	Check the repository status
Make sure there are no uncommitted changes before continuing.
git status
Expected result: Ideally, Git reports a clean working tree. If changes are present, save or commit them before proceeding.

⮚	Check the remote URL
Confirm that origin points to the correct GitHub repository.
git remote -v
Expected result: The output should show origin URLs for fetch and push.

⮚	Switch to main if necessary
If you are not already on main, switch to it. If your branch is master, use git switch master.
git switch main

⮚	Update local main before the demonstration
Bring the local main branch up to date before creating the demonstration commit.
git pull origin main

PART 3 – CREATE A LOCAL COMMIT ON THE SAME MAIN BRANCH

⮚	Create a sample file
		notepad local-notes.txt

⮚	Stage the file
git add local-notes.txt

⮚	Commit the local change
git commit -m "Add local notes for Experiment 5"

⮚	View the local commit
Display the latest commits.
git log --oneline	
PART 4 – CREATE A NEW REMOTE COMMIT ON GITHUB
⮚	Open GitHub
Open https://github.com/, sign in, and open the same Experiment4 repository.


⮚	Edit README.md on GitHub
Use the edit option for README.md and add the following line:
Remote changes for Experiment 5
PART 5 – FETCH THE LATEST REMOTE CHANGES

⮚	Fetch updates
Return to Git Bash and download the latest remote commits. Fetch updates remote-tracking references but does not merge them into the local branch.
git fetch origin

⮚	Check repository status
Check the working-tree status after fetching.
git status
PART 6 – REBASE THE CURRENT MAIN BRANCH
⮚	Confirm the current branch
git branch

⮚	Rebase main onto the updated remote main
Replay local commits that are not on origin/main on top of the latest remote main commit.
git rebase origin/main
git log –oneline

Expected result: If there are no conflicts, Git reports that the rebase completed successfully. If using master, run git rebase origin/master.



6th
PART 1 – OPEN GIT BASH AND ENTER THE REPOSITORY
➢ Open Git Bash
Open Windows Start, search for Git Bash, and launch it.

➢ Go to the Desktop folder
cd Desktop

➢ Enter the outer Experiment4 folder
cd Experiment4
➢ Enter the cloned repository
cd Experiment4

➢ Verify the repository
pwd
ls -a

Expected result: The .git directory and README.md should be visible.
PART 2 – CHECK STATUS, BRANCHES, AND REMOTE
➢ Check the repository status
git status

Expected result: Ideally, the working tree is clean. If you have changes you want to keep, commit or safely save them before continuing.
➢ List local branches
git branch

Expected result: The current branch is marked with an asterisk (*). Check whether the main branch is named main or master.
➢ Check the GitHub remote
git remote -v

Expected result: origin should show the GitHub repository URL for fetch and push.
PART 3 – UPDATE AND PREPARE THE MAIN BRANCH

➢ Pull the latest remote changes
git pull origin main

If using master, run git pull origin master. This helps ensure that the local main branch is up to date before creating the feature branch.
PART 4 – CREATE AND COMMIT A FEATURE
➢ Create feature-branch
git branch feature-branch
git switch feature-branch

This creates feature-branch from the current main branch and switches to it.
➢ Create a sample feature file
notepad book-search.txt

In Notepad, type a sample line such as: "Book search feature implementation". Save the file and close Notepad.
➢ Stage the file
git add book-search.txt

➢ Commit the feature
git commit -m "Add book search feature"

➢ Verify the feature commit
git log --oneline

Expected result: The new feature commit should appear in the recent commit list.
PART 5 – SWITCH BACK TO THE MAIN BRANCH
➢ Switch to main
git switch main

If the repository uses master, run git switch master instead.
➢ Confirm the current branch
git branch
PART 6 – MERGE WITH A CUSTOM COMMIT MESSAGE
➢ Merge feature-branch into main
git merge --no-ff feature-branch -m "Merge book search feature"
The --no-ff option requests a merge commit even if Git could fast-forward. The -m option supplies the custom merge commit message.
PART 7 – VERIFY THE MERGE
➢ Check repository status
git status

Expected result: The working tree should be clean.
➢ View the latest commit details
git show HEAD

Expected result: The latest commit details should include the custom message "Merge book search feature".
➢ List branches merged into the current branch
git branch --merged

Expected result: feature-branch should normally appear because it has been merged into the current branch.
PART 8 – PUSH THE MERGE TO GITHUB
➢ Push the updated main branch
git push origin main


⮚	Push the updated main branch 
git push origin main
