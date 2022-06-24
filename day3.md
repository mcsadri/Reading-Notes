# Day 3 Reading Notes

What is git?

- It's a version control system
- It lets multiple developers work on the same code
- A history of changes to your files
- The ability to view, apply, and remove those changes
- Keep all of your project files in one repository
- It makes collaboration possible!

Snapshots in time:

- Commits represent each successive version of a file or files
- Commits are the Git equivalent of Save As
- Each successive version create a new snapshot on the timeline of the project
- Git keeps track of what the file looked like at different points in time
- Each commit (snapshot) has a label that points to it
- HEAD = the label meaning "you are here"
- You can also assign messages to commits
- Messages are like writing a caption for your snapshot
- You use Git to take snapshot of your code at points in time
- Git keeps a history of those snapshots look like
- Git has a special label, called HEAD, that means "You Are Here"
- Usually you give a snapshot a label called a message

What is GitHub

- Not Git
- A way to share code with others
- An online place to store your code (Backup is good!)
- It uses Git to help you manage your team's work
  - Version tracking
  - Reviewing changes
  - Keep changes separate until you want to add them in

Git + github = awesome

- With Git (version control) and GitHub (online code storage), you can:
  - Have lots of team members work together on the same files, without messing each other up
  - Keep a history of each file over time
  - Work on code on you own computer, and sync it with what's online

What is a repository?

- A repo is a collection of files that you’ve told git to pay attention to
- Really large projects might have multiple repos for different parts of their system (i.e. front end vs back end)
- Repos can live on Github and/or on your computer

Creating a repo on GitHub

- Repos can be named anything
- But pick something meaningful
- Add a description
- Make Public
- Check: *Add a Readme file*
- Click: *Create repository*

Linking repos

- You just made a new repo
- Now we need to copy this repo onto our computer, and connect the two repos to each other
- If they're connected, they can give and receive code from the other repo
- We'll do this by **cloning**: from the cloud, to our local machine

Git cli cheat sheet

- `git clone {url}` to clone your repo from GitHub to your local machine
- `git add .` add all the files you changed to be tracked by git
- `git commit -m "message here"` - to commit your changes with a descriptive WHY comment
- `git push origin main` to send those changes to GitHub
