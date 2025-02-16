🔧 Mastering Version Control: A Deep Dive into SVN & Mercurial
Table of Contents

Introduction to Version Control Systems
Part 1: Subversion (SVN)

2.1 Overview & Key Features
2.2 How SVN Works
2.3 Essential SVN Commands & Workflow
2.4 Step-by-Step SVN Demonstration with Screenshots


Part 2: Mercurial (HG)

3.1 Overview & Key Features
3.2 How Mercurial Works
3.3 Essential Mercurial Commands & Workflow
3.4 Step-by-Step Mercurial Demonstration with Screenshots


Part 3: Creating a Git Repository and Hosting on GitHub Pages

4.1 Local Git Repository Setup
4.2 Uploading Your Presentation/Report
4.3 Linking to GitHub & Pushing Your Code
4.4 Configuring GitHub Pages and Sharing the URL


Conclusion & Best Practices


Introduction to Version Control Systems
Version Control Systems (VCS) are essential tools that help manage changes in software development. They enable collaboration, maintain a history of changes, and provide mechanisms to roll back to previous versions if needed.
Types of VCS:

Centralized Version Control Systems (CVCS):
Example: Subversion (SVN)
All versions are stored on a single central server.
Distributed Version Control Systems (DVCS):
Example: Mercurial (HG)
Every user maintains a complete copy of the repository, enabling offline work.

Why Use Version Control?

Tracks all changes with a detailed history.
Supports collaboration among multiple developers.
Facilitates branching, merging, and testing new features.
Enables rollbacks to previous versions if errors occur.


Part 1: Subversion (SVN)
2.1 Overview & Key Features of SVN

Centralized Repository:
All files and version history reside on a single server.
Revision-Based Tracking:
Every commit creates a new revision (e.g., r1, r2, r3).
Atomic Commits:
Changes are committed as a single transaction.
Branching & Tagging:
Directory-based branching and tagging for feature development.
Access Control & Locking:
Fine-grained permissions and exclusive checkout options.

2.2 How SVN Works

Central Repository:
The server holds all files and their history.
Working Copy:
Developers checkout the repository to make local changes.
Changes & Commits:
Edits are made locally and then committed back to the repository.
Updates & Merging:
Other users update their working copies, merging any changes.

2.3 Essential SVN Commands & Workflow
CommandDescriptionsvn checkout <repo-url>Get a working copy of the repositorysvn updateUpdate your working copy with the latest changessvn add <file>Add a new file to version controlsvn commit -m "Message"Commit changes with a descriptive messagesvn revert <file>Undo local changes before committingsvn statusShow modified or unversioned filessvn logView commit historysvn diffCompare differences between revisionssvn resolveResolve merge conflicts
SVN Workflow:
Checkout ➡️ Edit ➡️ Commit ➡️ Update ➡️ Resolve Conflicts
2.4 Step-by-Step SVN Demonstration with Screenshots
Step 1: Creating & Initializing a Repository
Command:
bashCopysvnadmin create C:\svn_repos\my_repo
Explanation:
Creates a new SVN repository at the specified location.
Screenshot:
[Insert Screenshot 1 here: Terminal showing the repository creation.]
Step 2: Checking Out a Repository
Command:
bashCopysvn checkout file:///C:/svn_repos/my_repo C:\Users\YourUser\my_working_copy
Explanation:
Checks out a working copy from the repository to your local machine.
Screenshot:
[Insert Screenshot 2 here: Terminal displaying the checkout process.]
Step 3: Making Changes & Committing
Commands:
bashCopyecho "Hello from SVN!" > C:\Users\YourUser\project\file.txt
svn add C:\Users\YourUser\project\file.txt
svn commit -m "Added file.txt with greeting message"
Explanation:
Creates a new file, adds it to version control, and commits the change.
Screenshots:

[Insert Screenshot 3 here: Showing file creation and svn add output.]
[Insert Screenshot 4 here: Showing svn commit output with new revision info.]

Step 4: Updating & Viewing Logs
Commands:
bashCopysvn update  
svn log
Explanation:
Updates your working copy and views the commit history.
Screenshots:

[Insert Screenshot 5 here: Terminal output of svn update.]
[Insert Screenshot 6 here: Terminal output of svn log.]

Step 5: Reverting Changes
Command:
bashCopysvn revert file.txt
Explanation:
Undoes local changes in file.txt before they are committed.
Screenshot:
[Insert Screenshot 7 here: Terminal showing the revert action.]
Step 6: Branching & Merging
Commands:
bashCopysvn copy file:///C:/svn_repos/my_repo/trunk file:///C:/svn_repos/my_repo/branches/feature-branch -m "Creating a feature branch"
svn merge file:///C:/svn_repos/my_repo/branches/feature-branch
Explanation:
Creates a branch (feature-branch) and later merges changes back.
Screenshots:

[Insert Screenshot 8 here: Showing branch creation.]
[Insert Screenshot 9 here: Showing merge output.]

Part 2: Mercurial (HG)
3.1 Overview & Key Features of Mercurial

Distributed Architecture:
Each user has a full repository copy.
Fast Performance:
Optimized for large codebases.
Simple Commands:
User-friendly commands similar to Git.
Atomic Commits & Branching:
Ensures commits are all-or-nothing and supports easy branching.
Scalability:
Suitable for projects of any size.

3.2 How Mercurial Works

Distributed Repositories:
Every developer works with a local full copy.
Committing Changes:
Local commits create new revisions.
Pull & Push:
Changes are exchanged between repositories.
Merging & Conflict Resolution:
Mercurial offers tools to merge changes seamlessly.

3.3 Essential Mercurial Commands & Workflow
CommandDescriptionhg initInitialize a new Mercurial repositoryhg clone <repo-url>Clone an existing repositoryhg statusShow the status of fileshg add <file>Add a new file for version controlhg commit -m "Message"Commit changes locally with a messagehg pullFetch changes from a remote repositoryhg pushPush local commits to the remote repositoryhg updateUpdate the working directory to a specified revisionhg mergeMerge changes from different brancheshg logView the commit history
Mercurial Workflow:
Clone ➡️ Edit ➡️ Commit ➡️ Push ➡️ Pull & Merge
3.4 Step-by-Step Mercurial Demonstration with Screenshots
Step 1: Creating & Initializing a Repository
Command:
bashCopyhg init my-hg-repo
Explanation:
Initializes a new Mercurial repository in the folder my-hg-repo.
Screenshot:
[Insert Screenshot 10 here: Terminal output showing successful initialization.]
Step 2: Adding & Committing Files
Commands:
bashCopyecho "Hello from Mercurial!" > newfile.txt  
hg add newfile.txt  
hg commit -m "Added newfile.txt"
Explanation:
Creates a new file, adds it to the repository, and commits the change.
Screenshots:

[Insert Screenshot 11 here: Terminal showing the creation and addition of the file.]
[Insert Screenshot 12 here: Terminal showing the commit details.]

Step 3: Cloning, Updating & Viewing Logs
Commands:
bashCopyhg clone https://example.com/repo  
hg pull  
hg update  
hg log
Explanation:
Clones a remote repository, pulls updates, applies them, and shows the log.
Screenshots:

[Insert Screenshot 13 here: Output from cloning.]
[Insert Screenshot 14 here: Output from pull/update.]
[Insert Screenshot 15 here: Output of hg log.]

Step 4: Branching & Merging
Commands:
bashCopyhg branch new-feature  
hg commit -m "Created new-feature branch"  
hg merge
Explanation:
Creates a new branch and demonstrates a merge process.
Screenshots:

[Insert Screenshot 16 here: Output showing branch creation.]
[Insert Screenshot 17 here: Output showing the merge command.]

Part 3: Creating a Git Repository and Hosting on GitHub Pages
4.1 Local Git Repository Setup
Step 1: Create and Initialize a Git Repository
Commands:
bashCopymkdir my-presentation
cd my-presentation
git init
Explanation:
Creates a new directory for your presentation/report and initializes an empty Git repository.
Screenshot:
[Insert Screenshot 18 here: Terminal output showing directory creation and git init.]
4.2 Uploading Your Presentation/Report
Step 2: Add Your Presentation/Report Files and Commit
Commands:
bashCopycp /path/to/your/presentation.html .
cp /path/to/your/report.md .
git add .
git commit -m "Initial commit: Add presentation and report files"
Explanation:
Copies your presentation and report files into the repository, stages them, and commits them.
Screenshots:

[Insert Screenshot 19 here: Terminal showing the file copy.]
[Insert Screenshot 20 here: Terminal output of git add and git commit.]

4.3 Linking to GitHub & Pushing Your Code
Step 3: Create a Repository on GitHub

Log in to GitHub via your web browser.
Create a new repository with the following settings:

Repository Name: my-presentation
Description (Optional): "Presentation and Report for Cloud Course."
Visibility: Public.
Do not initialize with a README.


Click Create Repository.

Screenshot:
[Insert Screenshot 21 here: GitHub repository creation page and the new repository homepage.]
Step 4: Link Your Local Repository to GitHub and Push
Commands:
bashCopygit remote add origin https://github.com/yourusername/my-presentation.git
git push -u origin master
Explanation:
Links your local repository with the remote GitHub repository and pushes your commits.
Screenshots:

[Insert Screenshot 22 here: Terminal output of adding the remote.]
[Insert Screenshot 23 here: Terminal output of a successful push.]
