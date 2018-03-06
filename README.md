Role Name
=========

 Ansible role to backup folders to tar.gz and copy them to amazon s3 bucket.

Requirements
------------

You just need your ansible installation nothing more.

Role Variables
--------------

Variables in default.yml:

1) Configure local backup path where the role will generate the tar for the specified directories.
local_backup_dir: /backups3

2) Configure environment for backups (demo, production, qa, etc)

customer: demo

3) AWS S3 bucket name

bucket_name: mybucket

4) Dictionary with each path to backup
paths_to_backup:
  path1:
    path: /var/www
    tag: www
  path2:
    path: /var/test_backup
    tag: test

5) AWS credentials

aws_access_key: aws_access_key
aws_secret_key: aws_secret_key

AWS access and secret key for account. This user must have read/write permissions for S3 service.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - backups3

License
-------

GPL v3

Author Information
------------------

Daniela Torres Faria
danielatorres@danielatorres.me
www.danielatorres.me
