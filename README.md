# **What**

This repository is an example to enable mirroring of Github repository to drupal.org project hosted on Gitlab.

# **Why**

We often host our Drupal.org projects on Github for better collaborations and workflows.

# **How**

This repository uses Github Actions workflow.

1. .github folder contains the workflows yml files.
2. gitlabintegrations.yml contains the github action configurations.

# **How to use**

1. Clone this repository and simply update the **.github/workflows/target_repo_url** to the URL for your destination repository.
2. Copy your SSH's PRIVATE key (for example: ~/.ssh/id_rsa) and add an **Actions secret** at https://github.com/<user_name>/<repository_name>/settings/secrets/actions
3. Make sure your Github profile's public ssh key is also added to your profile in git access on Drupal.org at https://www.drupal.org/user/<uid>/ssh-keys.

# **Credits**
1. https://github.com/marketplace/actions/mirroring-repository