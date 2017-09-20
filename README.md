# Project: Linux Server Configuration

Submission for "Project: Linux Server Configuration" for Udacity Full-Stack Program.

Author: Renee Iinuma

Date: 9/20/2017

## To Run

Navigate in browser:
IP Address: 34.208.252.236
URL: http://34.208.252.236

## Software Installed
- `virtualenv`
- Packages in requirements.txt of `https://github.com/rtiinuma/udacity_neighborhood.git`

## Configurations
- Updated packages with `sudo apt-get update` and `sudo apt-get upgrade`
- Changed SSH port in the `/etc/ssh/sshd_config` file to port 2200
- Configured firewall with command like `sudo ufw allow ssh`, `sudo ufw allow ntp`, `sudo ufw allow 2200/tcp`
- Created new user with `sudo adduser grader`
- Created key with `ssh-keygen` and moved public key to `.ssh/authorized_keys` for `grader` user
- Forced key-based auth by verifying `/etc/ssh/sshd_config` had `PasswordAuthentication no`
- Modified `/var/www/html/myapp.wsgi` with configurations for app
- Cloned `https://github.com/rtiinuma/udacity_neighborhood.git` and made minor code modifications (changing path to client_secrets, moving declaration of app.secret_key) for bug fixes
- Created `catalog.wsgi` and configured to activate venv
- Installed necessary packages with `pip install -r requirements.txt`
- Served app from `/var/www/html/udacity_catalog`

## Resources
- Amazon Lightsail
- Virtualenv
- StackOverflow