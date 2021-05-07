# **What**

This repository is an example to enable mirroring of Github repository to drupal.org project hosted on Gitlab. This will updated your Drupal.org's project repository with the changes in your Github repository, not vice-versa. This deployments/pushes can be check via "Actions" tab on your Github repository.

# **Why**

Sometimes, we host our Drupal.org projects on Github for better collaborations and workflows and we maintain it on Github and then push the changes to Drupal.org. But this is a manual task, so we need to find a solution which automates this process.

# **How**

This repository uses Github Actions workflow.

1. .github folder contains the workflows yml files.
2. gitlabintegrations.yml contains the github action configurations.

# **How to use**

1. Clone this repository and simply update the https://github.com/navneet0693/gitlab-github-integrations/blob/main/.github/workflows/gitlabIntegrations.yml#L15 to the URL for your destination repository.
2. Copy your SSH's PRIVATE key (for example: ~/.ssh/id_rsa) and add an **Actions secret** at https://github.com/<user_name>/<repository_name>/settings/secrets/actions
3. Make sure your Github profile's public ssh key is also added to your profile in git access on Drupal.org at https://www.drupal.org/user/<uid>/ssh-keys.
4. For example, you can see actions here: https://github.com/navneet0693/gitlab-github-integrations/actions

# **Credits**
1. https://github.com/marketplace/actions/mirroring-repository

# **Common questions**

##### 1.Does the non-primary branch also sync?
Yes, it non-primary branches also sync.

##### 2. What happens to branches that only live in Gitlab when a sync happens, are they preserved?
Unfortunately, it will be removed.

##### 3. What happens to a branch in Gitlab if a branch with the same name is created on GitHub? What should happen?
It remains same, but probably if the commits different then Github will prevail.

##### 4. Do tags also sync?
Yes, tags are also synced.

##### 5. What happens if I delete a tag or branch in Github?
It will be removed from Gitlab as well.

##### 6. What happens if I do some changes non-default branch?
Yes, they will be synced as well and will be present in both Github and Gitlab.

##### 6. Will the merge commits also be synced?
Yes, they will be synced as well automatically. Merge request, however will not be synced.
