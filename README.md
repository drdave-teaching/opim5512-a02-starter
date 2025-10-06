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

# GitHub classroom
Classroom assignment settings (A02)

Group assignment, team size = 2

Template repository: your A02 starter (with the files above)

Private repos, deadline set

Share the invite link with students

Student instructions (short)

Accept the Classroom invite → repo created for your team.

One partner creates a branch and opens a PR; the other reviews/comments/commits.

Ensure the pipeline runs and saves a PNG in A02-collab/figs/.

Wait for ✅ Autograding and ✅ Collaboration Check, then request instructor review.

Submit the PR URL (and latest commit hash) in HuskyCT.

TA grading “speed run”

Open PR → both checks green? ✅

Files changed only under A02-collab/**? ✅

Approve → merge → record score in HuskyCT.

If red, PR shows exactly which check failed (missing PNG / no partner participation).
