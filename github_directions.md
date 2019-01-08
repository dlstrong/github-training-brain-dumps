# Getting started with GitHub

## What is GitHub?

GitHub is a website that allows people to host programming projects online, with extra features to support users with collaboration and project organization.  There are a huge number of features and tools you can use in GitHub, but everyone needs to start with the same basic skills:

* Make a repository
* Get that repository onto your local machine
* Upload changes to your GitHub repository

You may be thinking that GitHub is something like a cloud storage service.  That isn't incorrect, but a very incomplete picture of what it can do.  Where GitHub differs between simple file storage is its version control capabilities.

## What is version control?

You are likely used to editing files in programs such as Word.  You add and change content in your file, saving as you go.  Every time you save you are writing over your previous file.  You can use the Undo function to back away from undesired changes.  This works pretty well most of the time.  However, having a queue of your 10 most recent changes may not be sufficient.  When it comes to writing code, there are very specialized needs that go well beyond the normal undo functions.  In addition, GitHub lets you identify synchronized changes acros several files at the same time; Word's versions are tracked independently of each other. However, this isn't meant to be a lesson on version control, so we'll gloss over a lot of this.

There isn't a one size fits all way of using version control, so don't look at these tools as dictating your workflow.  The goal is to fit them into your natual workflow, and you'll find youself using more features as the need arises and you become more comfortable.

At a mimimum, GitHub-style version control for programming (or for text files) means that you can:

* Create checkpoints for your code, representing milestones such as a completed feature or the end of you work day.
* View the differences between these checkpoints
* Work on different pieces or different ideas at the same time using branches
* Roll back to a previous version of a file
* Restore a deleted file

GitHub uses the git version control system and has added specialized tools on top of it.  

Here's the example repository that you'll be creating as we go through this lesson: https://github.com/dlstrong/swc-forklesson.  Take some time to look through the commits and files. You'll see that several different people have contributed to this one, and you can too. I'll show you how in a few minutes.

## Getting started with GitHub

Now that you know a little about what this is about, we can start stepping through the process.

### Create a GitHub account

Your first step will be to make a [GitHub account](https://github.com/).

Activity:  create account, about 5 minutes

### Optional:  sign up for a GitHub student developer pack

You can submit your request here: [https://education.github.com/pack/join](https://education.github.com/pack/join). There are various discounts, including free private repositories, available for students and academics. 

## Create a repository

You now have a GitHub account, and your account can have multiple repositories.  You should think of a repository as being a single project.  You can host files and folders in each repository.  Again, there's no hard rule on the boundaries for a repository, and you'll understand them better as you use more features of the platform.

Think of it this way:  this repository will turn into a directory on your computer.  You can store othe folders inside of it, but everything in there will travel together.  Again, this will make more sense once you see things in action.

Step through this process together as a class.

1. Log back into [GitHub](https://github.com/) if you need to
2. On the upper right hand corner of the page you'll see a + (plus) icon.  Click that + and select "New repository"
3. This will take you to a form where you'll add some information about your repository.
4. You'll need to add the following things:
	1. Repository name: your repository name should be something short but descriptive. You might want to name yours something like `datacarpentry-workshop-test`.  Do not include any spaces in your repository name.
	2. Description:  a sentence or two about what your repository will contain.  You might say "My test repository for the Data Carpentry workshop."
	3. Decide if you want to make your repository public or private.  You should be able to leave it as public for this workshop, but you can choose Private to make it viewable only to you and others that you invite.  Private repositories are part of a paid account, but are free (at the time of writing) with the student developer pack.
	4. Add a check next to "Initialize this repository with a README"
5. Click "Create repository" at the bottom of the page.


## What a repository page looks like

You should now see your repository's main page.  The two sections of this page that you should look at are the file section and your readme.

The file section is where you see the `README.md` file that you just made.  This can be hard to distinguish this section against others with only one file, but we'll be adding more.

The very last chunk of the page is the rendered contents of your readme file. This file is written in Markdown, which is a style of easily marking up text for web display.  We'll talk more about it when we start editing things.  The contents that were automatically added when you created the repository were the repository name and your description.  

## Editing your readme file

Any file with the name `README.md` (md is the extention for markdown files) will automatically be rendered and displayed at the bottom of your repository page.  We're going to pracice making some edits to it directly within the website.

Back in the file section, click on the `README.md` link.  This should take you to a new page where you again see the rendered contents of this file.  On the upper right side of this area (not the page) you'll see several buttons (do a page search for History to get to the right place) and several icons next to those buttons.  The pencil icon is the one that we want, hover over the icon and you should see that it says "Edit this file".  Go ahead and click that button now.

The screen will change to show the raw text behind the page (remember that we were seeing the rendered version), but you can also edit it!  Your text will look something like:

```
# Your repository name here
Some description here
```

The name of your repository is what will appear after the `#` and the description text will appear just below it.

Let's add some additional text to the end.

```
# swc-forklesson
This is a repository for Git lesson students to fork and submit pull requests to.

We'll take a look at the differences between submitting your own separate files as pull requests and collectively editing the contributors.txt file.
```

Once you're happy with your edits, scroll to the bottom of this page to see the Commit changes section. You can think of this like saving our changes to the file, but remember that in GitHub everything you do will have a bit of metadata lagniappe (a bit extra) along with it.  So we aren't just saving our file here, we're saving it along with a message about what we did.

Here you are offered two text fields.  The text box with one line you see just below "Commit changes" is the required commit message.  Version control isn't just about being able to track the changes made to a file, so this is where we can write a message about what this change is.  This message will be public and is meant to help you understand the context of the changes that you made.  The length is limited, so keep it to about 140 characters or less.  

Type in a commit message now:  "adding more information about this repository"

The larger text box just below is optional, and you can provide longer information about what's going on with your changes.  We'll leave this one empty.

Now we're ready to commit our changes!  We're going to use the default mode of `Commit directly to the master branch.`.  Now we're going to commit our changes with our new commit message. Click the big "Commit changes" button.

Once the page reloads, you'll see the new version of your readme file rendered with your additional text!

## Cloning the repo to your local machine

Again, everything with GitHub involved mostly normal things you'd do but with extra stuff and a different name.  Cloning means that you are downloading the repository to your computer, but keeping git aware of the files.  You aren's just downloading and unzipping a folder (which you can do), but downloading it in such a way that git will be watching the changes that you make to the files.

### Use a GitHub client of choice

There are two ways that you can interact with your GitHub repository:

1. On the website, which you've already done.  This is great for quick edits to plain text files, but doesn't allow you to execute any code, for example.
2. On your local machine. Where you have copies of your files that you edit, and then you publish your edits up to GitHub.  This will be the bulk of how you do your edits.

When working on your local copies, the website version of the files will remain the same until you push your changes.  Pushing changes is sort of like uploading your copies, but you're also sending along your commit messages and other metadata.  Again with that theme of "something normal with a bit extra."

As you might expect, you can't just download files to your machine like normal to have all the extra git things.  You need to use an application of some sort to handle the monitoring of local file changes and communication with GitHub.  There are several of these applications available, but two main free options:  the command line or a GUI application.  You can actually use both, so there's no pressure in choosing the one right thing at the start.  You may find that you prefer one but occasionally need the features of the other.  

Here are some examples of that:

* You are happy to work in the command line for the core tasks of committing and pushing, but find it easier to use the GUI application to review history, file differences, and roll back or restore previous versions.  The adrenaline rush of accidentally deleting all your project files can make it hard to focus and remember all the commands and steps for restoring them, and the GUI application can avoid some confusion.
* You prefer to use the GUI application for all your normal activity and this works just fine for most of your projects.  Occasionally you'll have a project that doesn't work well with the application (example: constantly making several hundred thousand files or more), and committing & pushing on the command line works better.

You'll find your own comfort space, and there's nothing wrong with using either method.  Again, focus first on what you can incorporate into your natural workflow, and then add complexity if the need arises.  This lesson will describe the process of installing and using GitHub desktop, but other Carpentries lessons will have directions for command line git.

### Install GitHub Desktop

This is a free application that is made by GitHub.  You can download it here:  [https://desktop.github.com/](https://desktop.github.com/).  

Once you download it, open the installer and follow all the normal installation methods.  Mac users, you'll need to drag the application to your Applications folder, and Windows users you should be able to follow all the exe direction.

After installing, go ahead and open it.  There are some major differences between the Windows and Mac versions, so there will be notes about each as we go along.  The biggest difference will be where you access menu items.  Mac users will have them at the top of the screen as normal.  Windows users will have a gear on the upper right of the screen.  There will also be differences in what things are called, e.g. Finder vs Explorer.

### Connect you account

Upon first opening it, Windows versions will go ahead and prompt you to log in.  (Do Macs? Not sure.)

Directions for logging in from the regular GUI:

* Windows: Under File, select Options.  
* Mac:  in the upper menu items, click on GitHub Desktop and select Preferences.  Click on the accounts tab if it isn't already selected.
* Choose the sign in option for to the GitHub.com option.
* Log in with your user name and password

### Do the cloning

From here, it will look pretty empty because you haven't added any repositories.  The good news is that we're finally ready to clone your repository!  Go back to your repository's website.  

You may have closed that website at this point, so we can practice how to find it from your github page.  Go to [GitHub.com](https://www.github.com/) and ensure that you are logged in.  Look on the right side of the page and you'll see a little pod called "Your repositories". You should see the name of your new repository in there.  Click on it and you'll be back.

At the main repository page, on the right you'll see a big green button that says "Clone or download".  Click that, and then "Open in Desktop".  Your operating system may ask to confirm that you want to open an application ("External protocol request" for windows and "Open it GitHub Desktop" for mac).  This will open up an info box in GitHub desktop.  You will want to review these options, so wait before clicking Clone!

The Repository URL will be be filled out for you, and you shouldn't change that. 

The Local Path will also be filled out for you.  By default, it will have a folder in your Documents directory called GitHub.  You can select a different folder if you want. 

Once you're happy with the local path that the repository will be saved in, you can click Clone.  We can confirm that our previous work on the website has been included by looking at the history.  On macs, the left panel will have two tabs for Changes and History.  On Windows these appear roughly in the middle of the window.  

Right now the Changes tab is empty because what we have locally matches exactly with what is on the website version.  Click on the History tab and you'll see two commits:  one for the initial commit where the readme file was created automatically at creation of the repository, and another where we added more info to our readme file.  You can click into those two commits to see the differences between the two files.

## Find the local copies

The interface is now a bit more interesting because you have a repository.  On the left side of the GitHub Desktop window it should say something like "Current Repository".  Clicking on that will toggle another window where it lists out all the git repositiories that it knows about.  It doens't go searching for local repositories on your computer, but you can have it managining multiple repositories.  

If you can't find this window, you can go up to View and select Show Repositories List.

Right now you may only see the one we just cloned, `swc-forklesson`.  Click on the name to go into that repository's view.

You can always use normal file navigation to find the folder that was just made, but there's a nice selection of shortcuts within the application.  These are in different spots depending on your OS.

* Mac:  click Repository and select Show in Finder.
* Windows:  click Repository and select Show in Explorer.

This will take you directly to your local folder for this repository.

## Fetch vs pull vs push vs commit
Some of the language Git and GitHub use can be easy to mix up. You'll see "fetch" and "pull" both mentioned in the desktop interface, and they sound like they mean something pretty similar! Here's what's actually going on with those words, though.

* Fetch: The system is checking what you have and what's in the remote location -- "fetching information." However, it's not actually changing any files yet.
* Pull: If the fetch indicates that there are things changed on the remote server that you don't have locally, you'll want to "pull" them to your local machine to work with the latest information.
* Push: If you've changed things on your computer that haven't been sent to GitHub, you'll want to "push" them from your computer to the remote system.
* Commit: A commit is the equivalent of a folder full of stuff that you use for "pushing" through the mail (or "pulling" from the remote server). You can have edits to several files in the same commit, so if you made a mistake you can remove the whole batch at once.

## Make changes on your local computer to send to GitHub

Next we're going to make some files locally and put them from your computer into GitHub.

For an example of how to collaborate with other people, we're going to create a new independent file to be shared with other people. 

* In order to make it easy to see what's going where, give the file your name: *your-name.txt* (in my case, dena-strong.txt).

Put some text in your file and save it in the local directory where your GitHub Desktop is watching. The changes in your file should show up in the Changes list in a few seconds. You'll see the file name, a green + sign by the file name, and a green preview of the text you entered.

Now that GitHub Desktop knows you've made a change, you can push it up to the server. However, if you do this:

* Under the Repository menu, choose Push.
* GitHub Desktop will process for a while and then (hopefully) report success.
* Check the website to see if it's there... 
* Nope, it's not there.

Remember commits? You have to tell GitHub Desktop that you want to make an envelope (a commit) for sending. Let's make another change in order to get a look at the bundling effect.

* Make an edit to README.md using your favorite text editor. Save the change.
* When it shows up in GitHub Desktop, it'll have a yellow icon (change) rather than green (new) beside it.
* You can include or exclude changes from your commit with the checkmark.
* In the left column, there's a text editing area at the bottom. Put a comment like "Adding my .txt file" in there.
* Click the blue Commit to Master button.

Check the website now... It's still not there. That's intentional. Making a commit collection is different than pushing to the remote server (or pulling from it).

* Notice the prompt in the top bar says "Push origin." If you click that, the push will happen.
* Refresh the website again and your edits will appear.

## Pulling a change to your local machine from the website

Now we know how to make changes on the website and locally, and them make them match up.  You may be wondering why someone would want to edit on the website.  Usually these are times when it is very convenient to, or you don't have access to nice Markdown previews.  For example, you may have discovered a typo that would be faster to fix in the website than launching your local instance of GitHub Desktop.  Or you may not be working on your computer with the local copies, so you can make the edits without having to install anything.

Go into your readme file on the website and launch the edit mode.  Remember that you do this by clicking on the name of the file and then the pencil icon.

Add something silly.

Acivity:

Take 5 minutes to write a silly joke (like a bad python pun) in your readme file.  Commit it into master using the website.

Example:

```
# your repository name
(your previous information here)

Why did the snake cross the road?  It hoped to put an arterial road between it and Python 2.
```

Now go back into your GitHub Desktop and look at the button you just used to push/sync.  It's likely to say "Fetch origin".  Click that button.

Now the button changes to say "Pull origin".  It should also have a down arrow and a 1.  This means that there is one commit to pull in (download) to your local version from the website.  

Click it again to pull that change in.  Once done, it should go back to saying "Fetch origin" with no numbers.

Now go into the history tab and you can see the silly joke that you added in.

## Reverting a change

Let's say this is now the next day and your advisor or dean wants to see your wonderful repository with the latest version of your work.  You are now rethinking your choice of having a silly joke there and want to revert that change.  

Go into your History tab and find the commit where you are adding the silly joke.  This should be the first one.  Right click on that change and select "Revert this commmit".  You'll see a new entry in the commit log where it has alread committed it for you.

Now open the readme file with a text editor.  You should see the offending joke is now gone.

Go ahead and push this change to GitHub, reload the repository page, and confirm that it is now gone.

## Recovering from destruction

So we've seen how to revert a commit that we've made, let's look at how you can recover lost work.

Go back into your file and delete all the contents.  

Now save it! See how there's no undo for this? Oh no!  

But not oh no!

Go check things out in GitHub Desktop.  You can see that your file is showing up as changed and all the cells in pink/red are deletions.  You can get rid of these changes.  

Right click on the change in the Changes tab and select "Discard Changes".  

Now go back to your file and re-open it.  You'll see that your work is now returned to you.

Activity 5 minutes:

Use your file browser to delete (drag them to the trash) all the files inside your repository folder (but not the folder itself).  Use the discard changes feature to restore all the files.  Mac users, you may see a `.DS_store` file show up.  You can safely add that to your ignored files.

Activity 5 minutes:  

Delete the entire folder from your computer and reclone the repository to your computer.  Hint: github destop will prompt you to reclone it.

## Issues and Pull Requests: Collaborating with other people

One of the best parts of GitHub is collaboration with other people. However, you don't necessarily want to give people all over the world access to read and write to your stuff. Issues and pull requests help with this. 

* Issues are when someone says "Here's a problem, but I don't have a solution to give you."
* Pull requests are when someone says "Here's a file with a solution. What do you think of it?"

Activities:
* Open some issues on your neighbors' repositories.
* Send me some pull requests for the forks you made of the original repository. 

##Branches: When you're testing things out
[[Note the Archive branch]]
