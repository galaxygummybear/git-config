===============================
Changing Git User Configuration
===============================

This guide explains how to change the default Git user configuration, how to set it for a specific repository, and how to amend commits and force push them.

Changing the Default Git User Configuration
-------------------------------------------

1. **Set the Global Username**:
   To set the default username for all repositories on your machine:

   .. code-block:: bash

      git config --global user.name "your_username"

2. **Set the Global Email**:
   To set the default email for all repositories:

   .. code-block:: bash

      git config --global user.email "your_email@example.com"

3. **Verify the Changes**:
   To check the global configuration:

   .. code-block:: bash

      git config --global user.name
      git config --global user.email

Setting Git User for a Specific Repository
------------------------------------------

1. Navigate to the repository's directory:

   .. code-block:: bash

      cd path/to/your/repository

2. Set the username and email for this specific repository:

   .. code-block:: bash

      git config user.name "your_username"
      git config user.email "your_email@example.com"

Amending Commits and Force Pushing
----------------------------------

1. **Amend the Last Commit**:
   If you've made a commit with the wrong user information, you can change the author of the last commit:

   .. code-block:: bash

      git commit --amend --reset-author

2. **Pushing After Amending**:
   If you've amended a commit and have already pushed commits to the remote repository before, you'll need to force push to overwrite the commit on the remote:

   .. code-block:: bash

      git push origin branch_name --force

   Replace `branch_name` with the name of the branch you're working on.

Note: Force pushing can overwrite changes on the remote repository. Use it with caution, especially if others are collaborating on the same branch.

