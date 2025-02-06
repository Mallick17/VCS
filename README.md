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

---
 # Generating SSH Key and Setting Up Access

Follow these steps to generate an SSH key on the Ansible-Master and set up access to the Worker node.

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
    
