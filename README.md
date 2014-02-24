ansible-git_application
=======================

A role for deploying applications from github

Actions

- Installs git
- Creates an <application user (if it doesnt already exist)
- Creates /opt/<application> (if it doesnt already exist)
- Pulls the code to the application folder, with the ref you want.

Requirements
------------

- SSH agent forwarding is enabled (for private github repos)

Role Variables
--------------

Below are all the variables used by the role, together an explanation, and their defaults.

`git_application_deploy_to`: The directory to deploy to - `/opt/myapplication`
`git_application_repo`: The URL of the repo - `git@github.com:mycompany/myapplication.git`
`git_application_version`: The branch / tag to deploy - `master`
`git_application_user`: The user that will own the code - `myuser`
`git_application_group`: The group the user will belong to - `myusergroup`

`git_application_pull_from_git`: Set to no if you want to skip this role entirely - `yes`

License
-------

MIT
