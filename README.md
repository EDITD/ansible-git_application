ansible-git_application
=======================

A role for deploying applications from github

Actions
-------

- Installs git
- Ensures an `application user` exists
- Ensures a `deploy_to` directory exists
- Pulls the code to the `deploy_to` directory, with the ref you want.

Requirements
------------

- SSH agent forwarding is enabled (for private github repos)

Role Variables
--------------

Below are all the variables used by the role, together an explanation, and their defaults.

- `git_application_deploy_to`: The directory to deploy to - `/opt/myapplication`
- `git_application_repo`: The URL of the repo - `git@github.com:mycompany/myapplication.git`
- `git_application_version`: The branch / tag to deploy - `master`
- `git_application_user`: The user that will own the code - `myuser`
- `git_application_group`: The group the user will belong to - `myusergroup`
- `git_application_pull_from_git`: Set to no if you want to skip this role entirely - `yes`

License
-------

MIT
