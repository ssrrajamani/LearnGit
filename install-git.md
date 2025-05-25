## Install Git on Mac OS X

There are several ways to install Git on a Mac. In fact, if you've installed XCode (or it's Command Line Tools), Git may already be installed. To find out, open a terminal and enter `git --version`

### Install using Mac Installer
1. Download the latest [Git for Mac installer](https://sourceforge.net/projects/git-osx-installer/files/).

2. Follow the prompts to install Git.

3. Open a terminal and verify the installation was successful by typing `git --version`

4. Configure your Git username and email using the following commands. These details will be associated with any commits that you create

    `git config --global user.name "Emma Paris"`

    `git config --global user.email "eparis@atlassian.com"`

5. (Optional) To make Git remember your username and password when working with HTTPS repositories, [configure the git-credential-osxkeychain helper](#install-the-git-credential-osxkeychain-helper)

### Install Git with Homebrew

1. `brew install git`

2. Open a terminal and verify the installation was successful by typing `git --version`

3. Configure your Git username and email using the following commands. These details will be associated with any commits that you create

    `git config --global user.name "Emma Paris"`

    `git config --global user.email "eparis@atlassian.com"` 
4. (Optional) To make Git remember your username and password when working with HTTPS repositories,[configure the git-credential-osxkeychain helper](#install-the-git-credential-osxkeychain-helper)

### Install the git-credential-osxkeychain helper
To work with a private repository over HTTPS, you must supply a username and password each time you push or pull. The git-credential-osxkeychain helper allows you to cache your username and password in the OSX keychain, so you don't have to retype it each time.


1. If you followed Homebrew instructions above, the helper should already be installed. Otherwise you'll need to download and install it. Open a terminal window and check:

    `git credential-osxkeychain`
    
        usage: git credential-osxkeychain <get|store|erase>
    If you receive a usage statement, skip to step 4. If the helper is not installed, go to step 2.

2. Use curl to download git-credential-osxkeychain (or download it via your browser) and move it to /usr/local/bin:

    `curl -O http://github-media-downloads.s3.amazonaws.com/osx/git-credential-osxkeychain`
    
    `sudo mv git-credential-osxkeychain /usr/local/bin/`

3. Make the file an executable:

    `chmod u+x /usr/local/bin/git-credential-osxkeychain`

4. Configure git to use the osxkeychain credential helper.

    `git config --global credential.helper osxkeychain`

### Install Git with Atlassian Sourcetree

Sourcetree, a free visual Git client for Mac, comes with its own bundled version of Git. You can [download Sourcetree here](http://www.sourcetreeapp.com/)

**To do source install and the installation for windows and linux can be found [here](https://www.atlassian.com/git/tutorials/install-git)**


