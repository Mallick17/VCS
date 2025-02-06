# Version Control System (VCS)
- VCS are a category of softwaretools that helps in recording made to files by keeping a track of modifications done in the code.
- Version control is also known as **Revision Control, Source Control & Source Code Management.**
- Version control is a component of software configuration management.
- Version Control includes viewing old versions & enables reverting a file to previous version.
- Benefits of version control systems:
  - A complete long-term change history of every file.
  - Branching and merging.
  - Traceability.
- There are three types of VCS
  - Localized VCS
  - Centralized VCS
  - Distributed VCS <br>
![VCS Types](https://github.com/user-attachments/assets/209f97a5-ca98-4963-90da-0bc05de5534f)
### Localized VCS
- It is one of the simplest forms and has a database that kept all the changes to files under Revision Control System (RCS).
- RCS is the most common VCS tools.
- It keeps patch sets (difference between files) in a special format on disk.
- By adding up all the patches it can then recreate what any file at anypoint in time.
### Centralized VCS
- Centralized VCS contain just one repository globally & every user need to commit for reflecting ones changes in the repository.
- It is possible for others to see your changes by updating.
- Two things are required to make your changes visible to others which are
  - You Commit
  - They Update
## Distributed VCS
- Distributed VCS contain multiple repositories.
- Each user has their own repo & working copy.
- When you update, you do not get others changes unless you have first pulled those changes into your repo.
- To make changes visible to others, 4 things are required
  - You Commit
  - You Push
  - They Pull
  - They Update
- The most popular distributed VCS are Git, Mercurial, BitBucket.
- They helps us overcome the problem of single point of failure.


# Git
**GIT = Global Information Tracker**
- Git is open source, distributed version control tool to achieve collabration with each & every developers. where we can track each & every modification or changes & we can have more control over each version of the code.
- Benefits are **Feature Branch Overflow, Distributed Development, Pull Requests, Community, Faster Release Cycle**
## Git Commands & Explaination

| Keywords                     | Description                                                                                                             |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------- |
| git                          | Open-source distributed version-control system, used to store code in repositories                                      |
| GitHub, GitLab and Bitbucket | Platform for hosting and collaborating on Git repositories                                                              |
| staging                      | Proposed files/directories that you'd like to commit                                                                    |
| commit                       | Saving all staged files/directories to your local repository                                                            |
| branch                       | An independent line of development, so you can develop features isolated from each other. Master branch is the default. |
| clone                        | Local version of a repository, including all commits and branches                                                       |
| remote                       | Common repository on eg. Github that all team members to keep that changes in sync with                                 |
| fork                         | Copy of a repository owned by a different user                                                                          |
| pull request                 | A method of submitting contributions to a repository                                                                    |
| HEAD                         | Represents your current working directory                                                                               |

### Configuration

| Key/Command                              | Description                                         |
| ---------------------------------------- | --------------------------------------------------- |
| `git config --global user.name [name]`   | Set author name to be used for all commits          |
| `git config --global user.email [email]` | Set author email to be used for all commits         |
| `git config color.ui true`               | Enables helpful colorization of command line output |

### Core Commands

| Key/Command                 | Description                                              |
| --------------------------- | -------------------------------------------------------- |
| `git init [directory]`      | Creates new local repository                             |
| `git clone [repo]`          | Creates local copy of remote repository                  |
| `git add [directory]`       | Stages specific [directory]                              |
| `git add [file]`            | Stages specific [file]                                   |
| `git add -A`                | Stages all changed files                                 |
| `git add .`                 | Stages new and changed files, NOT deleted files          |
| `git add -u`                | Stages changed and deleted files, NOT new files          |
| `git commit -m "[message]"` | Commit everything that is staged                         |
| `git status`                | Shows status of changes as untracked, modified or staged |

### Synchronization of Changes

| Key/Command   | Description                                                                           |
| ------------- | ------------------------------------------------------------------------------------- |
| `git fetch`   | Downloads all history from the remote branches                                        |
| `git merge`   | Merges remote branch into current local branch                                        |
| `git pull`    | Downloads all history from the remote branch and merges into the current local branch |
| `git push`    | Pushes all the commits from the current local branch to its remote equivalent         |

*Tip: `git pull` is the combination of `git fetch` and `git merge`*

### Undo Changes

| Key/Command                 | Description                                                                                 |
| --------------------------- | ------------------------------------------------------------------------------------------- |
| `git checkout -- [file]`    | Replace file with contents from HEAD                                                        |
| `git revert [commit]`       | Create new commit that undoes changes made in [commit], then apply it to the current branch |
| `git reset [file]`          | Remove [file] from staging area                                                             |
| `git reset --hard HEAD`     | Removes all local changes in working directory                                              |
| `git reset --hard [commit]` | Reset your HEAD pointer to previous commit and discard all changes since then               |

### Branches

| Key/Command                | Description                        |
| -------------------------- | ---------------------------------- |
| `git branch [branch]`      | Create a new branch                |
| `git checkout [branch]`    | Switch to that branch              |
| `git checkout [branch] -b` | Create and checkout new branch     |
| `git merge [branch]`       | Merge [branch] into current branch |
| `git branch -d [branch]`   | Deletes the [branch]               |
| `git push origin [branch]` | Push [branch] to remote            |
| `git branch`               | Lists local branches               |
| `git branch -r`            | Lists remote branches              |
| `git branch -a`            | Lists local and remote branches    |

### History

| Key/Command                | Description                                                      |
| -------------------------- | ---------------------------------------------------------------- |
| `git log`                  | Lists version history for the current branch                     |
| `git log --author=[name]`  | Lists version history for the current branch from certain author |
| `git log --oneline`        | Lists compressed version history for the current branch          |
| `git show [commit]`        | Outputs metadata and content changes of the specified commit     |
| `git blame [file]`         | Shows who changed what and when in file                          |


---
 # Generating Git SSH Key and Setting Up Access
 - An SSH key is an access credential for the SSH (secure shell) network protocol. This authenticated and encrypted secure network protocol is used for remote communication between machines on an unsecured open network. SSH is used for remote file transfer, network management, and remote operating system access. The SSH acronym is also used to describe a set of tools used to interact with the SSH protocol.
 - The key pair contains a public and private key. The private vs public nomenclature can be confusing as they are both called keys. It is more helpful to think of the public key as a "lock" and the private key as the "key". You give the public 'lock' to remote parties to encrypt or 'lock' data. This data is then opened with the 'private' key which you hold in a secure place.
- Follow these steps to generate an SSH key

## Generate SSH Key on Linux

- **Open a terminal in Git Bash or Linux and execute the following command:**

  ### 
  ```sh
  ssh-keygen
  ```
- **You will then be prompted to "Enter a file in which to save the key."**
  - You can specify a file location or press “Enter” to accept the default file location.
    ```sh
    Enter a file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]
    ```
- **The next prompt will ask for a secure passphrase. A passphrase will add an additional layer of security to the SSH and will be required anytime the SSH key is used. If someone gains access to the computer that private keys are stored on, they could also gain access to any system that uses that key. Adding a passphrase to keys will prevent this scenario.**
  ```sh
  > Enter passphrase (empty for no passphrase): [Type a passphrase]
  > Enter same passphrase again: [Type passphrase again]
  ```
  
- **List all files in the current directory to verify the creation of the key**
  ```sh
  ls -a
  ```
- Navigate to the .ssh directory
  ```sh 
  cd .ssh
  ```
- View the contents of the generated SSH key
  ```sh
  cat id_rsa
  ```
- **Add the new SSH key to the ssh-agent**
  - The ssh-agent is another program that is part of the SSH toolsuite. The ssh-agent is responsible for holding private keys. In addition to holding private keys it also brokers requests to sign SSH requests with the private keys so that private keys are never passed around unsecurly.
  - Before adding the new SSH key to the ssh-agent first ensure the ssh-agent is running by executing:
    ```sh
    $ eval "$(ssh-agent -s)"
    > Agent pid 59566
    ```
  - Once the ssh-agent is running the following command will add the new SSH key to the local SSH agent.
    ```sh
    ssh-add -K /Users/you/.ssh/id_rsa
    ```
  - The new SSH key is now registered and ready to use.
    
