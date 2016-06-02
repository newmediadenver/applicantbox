# devbox
Vagrantfile and wrapper script to facilitate local development
## Usage
### Spin up the box
```
vagrant up
```
### Execute a build action for a site
```
./dev [ACTION] [SITE]
```
### Available Actions:

* create - provision a site from scratch onto the VM
* update - run an update deployment on the VM
* backup - create a backup archive and upload to S3
* delete - delete the site from the VM
* switch - set the site as the active site for nginx to serve. useful for running multiple sites on the same VM
* list   - list site currently on the VM, does not require [SITE] to run

Example:
```
./dev create qxnews
```

### Move project files between Host and VM
By default assumes site is cloned to directory ~/sites/sitename. This can be modified in the syncto/syncfrom scripts.
```./syncto [SITE]``` - update files from ~/sites/sitename on the Host to /var/www/sitename on the VM
```./syncfrom [SITE]``` - update files from /var/www/sitename on the VM to ~/sites/sitename on the Host.

### Additional Vagrant Commands
```vagrant ssh``` - log into the VM

```vagrant suspend``` - suspend the VM

```vagrant destroy``` - destroy the VM

```vagrant box update``` - update the base box if a new one is available
