## Setting up a repository

### git init

**`git init`**  The current directory from which the command is executed becomes the git repository


**`git init <repo name>`** Creates a new empty directory and makes it a git repository


> Executing `git init` or `git init <repo name>` creates a .git subdirectory in their git repository directory, which contains all of the necessary Git metadata for the new repository. This metadata includes subdirectories for objects, refs, and template files.

Ex: `git init sample` will create a new directory sample if not exists and create a `.git` subdirectory within the sample git repository. 

**Without the .git subdirectory sample directory is just a folder and not a git repository.**

    -- sample
        -- .git (folder)
            -- config      
            -- description 
            -- HEAD        
            -- hooks       
            -- info        
            -- objects     
            -- refs


Now for a reason, the user doesn't want the .git subdirectory created inside the sample directory. Instead wants the .git directory to be created in seperate place.

**`git init --separate-git-dir=`** 

    By default, git init will initialize the Git configuration to the .git subdirectory path. The subdirectory path can be modified and customized using '--separate-git-dir' argument

Ex: `git init sample --separate-git-dir=git_configs/sample` will  store the contents of .git of sample repository inside git_configs/sample

    -- git_configs
        -- sample
            -- config      
            -- description 
            -- HEAD
            -- hooks       
            -- info        
            -- objects     
            -- refs
    -- sample
        -- .git (file)

> **What's this?**  For the curiosity check what is present in .git file

>You can call git init --separate-git-dir on an existing repository and the .git dir will be moved to the specified  path.


---

#### Templates 
Allow you to initialize a new repository with a predefined .git subdirectory. You can configure a template to have default directories and files that will get copied to a new repository's .git subdirectory.

Ex: `git init sample --template=template1`

    -- template1
        -- file1.txt
    -- sample
        -- .git
            -- file1.txt
            -- config      
            -- description 
            -- HEAD
            -- hooks       
            -- info        
            -- objects     
            -- refs

---
---
