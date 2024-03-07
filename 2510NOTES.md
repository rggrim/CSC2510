When you commit, the updates exist on the local devoie in your .git file
commit - save to your local repository, in your .git file
push - save to shared repository (server)
pull/fetch - check for updates
squash - shove all the commits together, and you can no longer access the commit history or revert commits
remote repository - any repository that is not your local repo, including repos on other collaborator's devices and the shared gitHub repo

four ways to resolve conflicts when pushing to origin
 - accept your own (resolve with mine)
 - resolve with theirs
 - resolve with both                    # how does this work???
 - resolve with none (get rid of both)

When working with different branches, you can create a merge commit
back into the main branch. This saves the merge to your local repo.


**BASH COMMANDS**
pwd                 - Print Working Directory, shows you where you currently are
ls                  -  shows every file in the directory except for hidden files
ls -a               - shows every file, INCLUDING hidden files
ls -ltr             - shows your permissions, w for write, d is for denied?, x for execute, r is for read
                      also shows the name of the owner, file size, modification date and time, and file name
                      r:read - 4 
                      w:write - 2
                      x:execute - 1
                      ___________   ______________    ____________   there are 3 positions for permision groups
                      **OWNER**     **OWNER GROUP**   **WORLD**
chmod _ _ _ filename - gives permisions to file or directory
chown username filename - may need to use sudo but it will transfer ownership of filename to username
ls -ltr | tail -n 3 - shows permissions for the tailing 3 files in the creation order
p *                 - returns everything that starts with a p?
clear               - clears your screen
cd                  - change directory
cd ..               - moves you up into the parent folder of wherever you currently are in the directory
nano                - opens text editor
nano fileName.fileType - opens text editor with filename
cat myFile.txt      - prints whats in the text file
head / tail myFile.txt - prints the first few or last lines of the text file
rm myFile.txt       - deletes the file
rm -r dirName       - deletes directory/folder/file
rm something*       - removes everything with a title containing "Something" followed by anything in pwd
mkdir               - makes a directory
mv dirName newName  - renames folder or file to newName
mv dirname Directory/newName - moves dirName into Dorectory, replacing dirName with the name newName
touch               - to create a new file
&&                  - allows us to execute multiple actions in one line
whoami              - returns current working User
sudo whoami         - doesn't work for Windows
tail --help         - prints out details about command options for "tail"
cp fileName newFile - copies fileName into a new file


**GIT CLI**
git init -b main    - creates a .git/ folder in your directory and names it main
git status          - fetches to check if you're up to date
git branch -m newName - renames currently checked out branch to newName
git add config.json - stage config.json
git add *           - stages all files with uncommitted changes 
git add *.txt       - stages all .txt files with uncommited changes
git commit -m ""    - commits all staged files with a message of your choice between the parentheses
git log             - view all commits and displays hashes for the commits!
git clone sshLink   - will clone the repo at the end of the link, putting it into a folder with the name        
                      of the cloned repo
git checkout
git push
git checkout -b newBranchName
git merge branchName
git pull

**UBUNTU CLI**
sudo __my command__             - S.witch U.ser, then D.O., for when you don't have proper permissions for my_command
sudo apt-get update             - do before every install to make sure your system is up to date
sudo apt-get install package name - to install new package 
cat myFile.txt >> combined.txt  - creates newfile combined.txt and puts myFile.txt into it
cat myFile2.txt >> combined.txt - puts both files into combined.txt

cat myFile.txt > combined.txt
cat myFile2.txt > combined.txt - overwrites combined.txt with myFile2.txt

grep -l "phrase" *              - searches all files in pwd for phrase and returns the names of those files
grep -r myPhrase                - searches inside ???
ls | grep simpson               - looks at every file returned by ls and returns files containing simpson
| (piping)                      - takes results from left and uses them for command on the right
grep 'myPhrase' filename        - looks for lines with myPhrase in filename
echo                            - what does echo do?
top                             - displays running processes, constantly updating
awk                             - query language for CLI 
awk '{print $2,$4}' filename    - prints everything in columns 2 and 4 in filename
awk '/phrase/ {print}' filename - looks for phrase in filename and prints line containing phrase
sed 's/phrase/newphrase/' filename - prints new phrase instead of phrase in filename
sed 's/phrase/newphrase/g' filename - universally prints new phrase in filename where phrase is present
curl https://.....              - prints website page contents



**JSON FILE STRUCTURE:**
json files are made up of key value pairs!

[
        {"firstname":"Riley","lastname":"Grimaud"},
        {"firstname":"Daniel","lastname":"Selvidge"}
]

