## Source Code Management (SCM)

Source code management (SCM) is used to track modifications to a source code repository. SCM tracks a running history of changes to a code base and helps resolve conflicts when merging updates from multiple contributors. SCM is also **synonymous with Version control**. 

## Importance of SCM

Two developers are working on two different features but both share the same code file

Before the adoption of SCM this was a nightmare scenario. Developers would edit text files directly and move them around to remote locations using FTP or other protocols. Developer 1 would make edits and Developer 2 would unknowingly save over Developer 1’s work and wipe out the changes. 

SCM safeguards work by tracking changes from each individual developer and identifying areas of conflict and preventing overwrites. SCM will then communicate these points of conflict back to the developers so that they can safely review and address.

This foundational conflict prevention mechanism has the side effect of providing passive communication for the development team.

## Benefits of SCM

1. Provides a detailed historical record of the projects life is created. This historical record can then be used to ‘undo’ changes to the codebase.

2. A clean and maintained SCM history log can be used interchangeably as release notes.

3. SCM will reduce a team’s communication overhead and increase release velocity. Without SCM development is slower because contributors have to take extra effort to plan a non-overlapping sequence of develop for release. 

## Best Practices

### Commit Often
Each commit is a snapshot that the codebase can be reverted to if needed. Frequent commits give many opportunities to revert or undo work. 

### Ensure working with latest version

It’s easy to have a local copy of the codebase fall behind the global copy. Make sure to git pull or fetch the latest code before making updates. This will help avoid conflicts at merge time.

### Make detailed note

Commit log messages should explain the “why” and “what” that encompass the commits content.

### Review changes before committing

SCM’s offer a ‘staging area’. The staging area can be used to collect a group of edits before writing them to a commit. The staging area can be used to manage and review changes before creating the commit snapshot. Utilizing the staging area in this manner provides a buffer area to help refine the contents of the commit.

### Use branches

Branches enable multiple developers to work in parallel on separate lines of development. When development is complete on a branch it is then merged into the main line of development.