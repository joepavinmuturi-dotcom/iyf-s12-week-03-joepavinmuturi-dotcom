# Terminal Log

## Navigation
- `pwd` - printed my current directory
- `ls` - listed files in the current directory
- `cd ~/Documents` - moved into Documents
- `cd ..` - moved up one level
- `cd ~` - returned to home

## Project structure
- `mkdir -p my-project/src/{css,js,images} my-project/docs my-project/tests` - created nested folders
- `touch my-project/README.md` - created an empty README
- `ls -R my-project` - showed the full tree to verify

# File operations

## Files
- `touch index.html` - created an empty file
- `cat index.html` - showed contents (empty)
- `cp index.html backup.html` - copied the file
- `mv backup.html docs/` - moved the copy into docs
- `mv index.html home.html` - renamed the file
- `rm home.html ` - deleted the file

## Directories
- `cp -r src/ src-backup/` - copied a folder
- `mv src-backup/ archive/` - renamed the folder 
- `rmdir archive/` - failed because the folder was not empty
- `rm -r archive/` - deleted the folder and its contents

## Useful Commands
- `find . -name "*.html" | wc -l` - 4 HTML files
- `grep -rl "contact" .` - found in index.html, contact.html
- `wc -l styles.css` - 120 lines
- `history | tail -10` - showed my last 10 commands

## Shell Script
- `touch new-project.sh` - created the script file
- `code new-project.sh` - opened it in VS Code and pasted the script
- `chmod +x new-project.sh` - made it executable
- `cd ~/terminal-practice` - moved to my scratch folder
- `bash ~/iyf-s12-week-03-joepavinmuturi-dotcom/new-project.sh my-awesome-app` - created the project structure
- `ls -R my-awesome-app` - checked that all folders and files were created
- Ran the script with no name - printed the Usage message and exited

## What the script does
- `$1` holds the project name I type after the script name
- `[ -z "$PROJECT_NAME" ]` checks whether the name is empty
- `mkdir -p` creates the nested folders in one command
- `echo "# $PROJECT_NAME" > README.md` writes a heading into the README

## git basics
- `git status` - checked what had changed
- `git add styles.css` - staged my CSS change
- `git commit -m "Style: add navigation hover underline"` - committed the hover style
- `git add styles.css` - staged my second CSS change
- `git commit -m "Fix: correct responsive breakpoint for projects grid"` - committed the breakpoint fix
- `git log --oneline` - listed my commits in short form
- `git push` - uploaded my commits to GitHub