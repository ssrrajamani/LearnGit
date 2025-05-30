## What is Git?
By far, the most widely used modern version control system in the world today is Git. Git is a mature, actively maintained open source project originally developed in 2005 by Linus Torvalds, the famous creator of the Linux operating system kernel.

Having a **distributed architecture**, Git is an example of a DVCS (hence **Distributed Version Control System**). Rather than have only one single place for the full version history of the software as is common in once-popular version control systems like CVS or Subversion (also known as SVN), in Git, every developer's working copy of the code is also a repository that can contain the full history of all changes.

### What is Distributed Version Control System?


A Distributed Version Control System (DVCS) is a type of version control system where every contributor (user) has a full copy of the entire code repository, including the complete history of all changes, stored locally on their machine.

Unlike Centralized Version Control Systems (CVCS) (e.g., Subversion), which rely on a single central server, DVCS tools (like Git) allow independent work, offline commits, and collaborative branching/merging without always needing access to a central server.
Being distributed enables significant performance benefits as well.

For example, say a developer, Alice, makes changes to source code, adding a feature for the upcoming 2.0 release, then commits those changes with descriptive messages. She then works on a second feature and commits those changes too. Naturally these are stored as separate pieces of work in the version history. Alice then switches to the version 1.3 branch of the same software to fix a bug that affects only that older version. The purpose of this is to enable Alice's team to ship a bug fix release, version 1.3.1, before version 2.0 is ready. Alice can then return to the 2.0 branch to continue working on new features for 2.0 and all of this can occur without any network access and is therefore fast and reliable. She could even do it on an airplane. When she is ready to send all of the individually committed changes to the remote repository, Alice can "push" them in one command.