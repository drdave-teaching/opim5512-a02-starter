# opim5512-a02-starter
This is the starter repo for students to clone to their own repository. 

## First, make sure you have GitHub CLI installed (should only need to do this once.)
```bash
# Install GitHub CLI (Windows)
winget install GitHub.cli

# Verify
gh --version

# Login (follow the browser flow)
gh auth login
# → GitHub.com → HTTPS → "Login with a web browser"
```

## Now you can clone it!

```bash
cd $HOME\Desktop

# set params
$ORG      = "drdave-teaching"
$ASSIGN   = "a01"        # change to a02 when needed
$NETID    = "dww05002"   # student edits this
$TEMPLATE = "$ORG/opim5512-$ASSIGN-starter"
$NEWNAME  = "$ORG/opim5512-$ASSIGN-$NETID"

# create a new repo from the template and clone it here
gh repo create $NEWNAME --template $TEMPLATE --private --clone

# enter the new repo and start a working branch
cd ".\opim5512-$ASSIGN-$NETID"
git switch -c "$ASSIGN/$NETID-work"
git push -u origin HEAD
```
