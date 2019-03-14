Repository support
=========

This role allows the machine to access a remote git repository. In order to support this, it will install git and upload a deployment key to the repository. At the moment only bitbucket repos are supported.

Requirements
------------

This role needs the `bitbucket_deployment_key` module to be available. In order to make this module available, you need to clone `git@github.com:tinydesk/ansible-modules-extras.git` and put the resulting directory in the environment variable `ANSIBLE_LIBRARY`.

Role Variables
--------------

- `repository_names`: The names of the bitbucket repositories in the form `<user>/<repo>`
- `bitbucket_username`: The name of a bitbucket user with access to the repository
- `bitbucket_password`: The password for the bitbucket user
- `ssh_key_path`: Path to the local ssh key so that you can access the newly created deploy user

Note that in order to protect the password it is recommended to use `ansible-vault`.

Dependencies
------------

- geerlingguy.git

Example Playbook
----------------

License
-------

MIT
