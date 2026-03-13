1.3 Git Configuration (git config)

 

Git is a distributed version control system designed to track changes in files and maintain a complete history of modifications within a repository.

To achieve this, Git records information about who made the change and when the change occurred.

 

Before starting to work with Git, it is important to configure your identity. This identity is attached to every commit you make, allowing Git to maintain proper authorship information.

 

The git config command is used to set configuration values such as the user name and email address associated with your commits.

 

Configure User Identity

 

Use the following commands to configure your Git identity:

 


bash
⧉
git config --global user.name "Your Name"
git config --global user.email "you@example.com"


 

The --global flag applies these settings to all Git repositories on your system. This means every repository you work with will use this identity by default.

 

If needed, different configuration values can also be set for individual repositories.

 

Verify Git Configuration

 

You can verify the configured identity using the following command:

 


bash
⧉
git config -l


 

Example output:

 

user.name=Your Name

user.email=you@example.com

 



This command lists all the configuration settings currently applied in Git.

 



Note:

If you are working on multiple projects (for example personal and company projects),  you may want to configure different email addresses for different repositories.
