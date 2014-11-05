# Learn Git (Command Line) In 10 Mins

Git tracks changes on a file. It's similar to the way Google Docs tracks revision history. If you've never seen Google Docs revision history, check that out before reading this. This will make more sense.

This is a Mac / Linux tutorial. If you have Windows you need to download [this](http://msysgit.github.io/) and launch git bash and then do the same stuff.

### Step 0: Install Git
[Here for Mac](http://git-scm.com/book/en/v2/Getting-Started-Installing-Git#Installing-on-Mac)

### Step 1: Open terminal
Like Applications > Terminal. No trickery here.

### Step 2: Get To Your Project
```
cd /directory/of/your/project
```
Example (assuming I created a folder called fun stuff on my desktop):
```
cd /Users/benpaster/Desktop/funStuff
```
In terminal, I can use `~` to get to my home directory which is `/Users/benpaster/`
```
cd ~/Desktop/funStuff
```
You can also drag and drop:

<img src="http://on.simpler.im/19KLC+" height="400px" />

### Step 3: Tell Git To Start Tracking

**SKIP THIS STEP IF YOU ARE USING SOMEONE ELSE'S CODE WHO WAS ALREADY USING GIT. THEY DID THIS.**

Make sure you're in the directory we just cd'd (changed directory) to. 
```
git init
```

### Step 4:
Make changes to the files!

### Step 5: 
See what files you changed (never leave your project directory!)
```
git status
```

### Step 6:
Tell git you're done with changes to those files for now. 
"." means everything that just showed up in git status
```
git add .
```
Optionally, add one/less than all files
```
git add file1.something file2.something
```

### Step 7: 
Commit those changes. This tells git that the files you just added are really done and can now be grouped into one commit (usually a part of a feature or something like that).
```
git commit -m "first update!"
```

### Step 8:
See your commit
```
git log
```

## Pushing Code to a Remote Location
While GitHub will be the example, this is not a GitHub tutorial. GitHub has a lot of features that this does not cover.

### Step 0:
If you used someone else's code, there is a 99% chance you can simply do this:
```
git push origin
```
But it might not be called origin, maybe... so check:
```
git remote
```

Aaaanddd, you're done. Stop reading. woo.

### Step 1: Add Remote Repository
```
git remote add origin https://username@github.com/username/repo.git
```
You can find the full URL here on GitHub:
<img src="http://on.simpler.im/15VRX+" height="200px" />

### Step 2: Send your code up to the remote repo
```
git push origin
```
### Step 3: Get your code again later
```
git pull origin
```
