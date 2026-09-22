# my_Practical2

Practical: Git Commands

Aim: To perform Git operations:

Clone a remote repository
Create a file locally, commit it, and push to GitHub
Pull remote changes into the local repository


What is Git?

Git is a distributed version control system used to track changes in source code and manage project versions.

Main uses:
Store project history
Collaborate with multiple developers
Restore previous versions
Upload/download code from GitHub
What is GitHub?

GitHub is a cloud platform that stores Git repositories online.

Relationship:

Local Computer  ←→  Git  ←→  GitHub (Remote Repository)
I. Clone the Remote Repository
Command:
git clone https://github.com/byteWithRiddhi/my_Practical2.git
Explanation:
git clone → Copies an existing remote repository to your local computer.
URL → Address of repository on GitHub.
What happened in your practical:

Git downloaded the repository and created a local folder.

Example:

Before:

PC

After:

PC
└── my_Practical2

Move into repository:

cd my_Practical2

Meaning:

cd = Change Directory
Enter the cloned folder
II. Create a New File Locally, Commit and Push
Step 1: Create file

Command: 

touch newfile.txt

Explanation:

Creates an empty text file.

Result:

my_Practical2
└── newfile.txt

Step 2: Add content

Command:

echo "This is a new file" > newfile.txt

Explanation:

echo → Prints text
> → Writes text into file

File content:

This is a new file

Step 3: Add file to staging area

Command:

git add newfile.txt

Explanation:

Git does not track files automatically.

git add moves changes to the staging area.


Flow:

Working Directory -> git add -> Staging Area

Your warning:
LF will be replaced by CRLF

Meaning:

Windows uses CRLF line endings
Linux uses LF
Not an error

Step 4: Commit changes

Command:

git commit -m "Added new file"

Explanation:

Creates a permanent snapshot of current changes.

Options:

commit → Save changes
-m → Commit message

Example:

Commit:
"Added new file"

Flow:

Working Directory
->
Staging Area
->
Commit

Step 5: Push changes to GitHub

Command:

git push origin main

Explanation:

Uploads committed changes from local repository to GitHub.

Breakdown:

git push → Send changes

origin → Remote repository

main → Branch name

Your output:

Writing objects: 100%
To https://github.com/...

Meaning:
✅ Files uploaded successfully

Flow:

Local Repo
      ->
git push
      ->
GitHub Repository

III. Pull Remote Changes

Command:

git pull origin main

Explanation:

Downloads latest changes from GitHub and merges into local repository.

Breakdown:

pull = fetch + merge

origin = remote

main = branch

Your output:

Already up to date.

Meaning:
No new changes existed on GitHub.

Flow:

GitHub
 ->
git pull
 ->
Local Repository


Commands Summary
git clone <repository_url>

cd repository_name

touch newfile.txt

echo "This is a new file" > newfile.txt

git add newfile.txt

git commit -m "Added new file"

git push origin main

git pull origin main
