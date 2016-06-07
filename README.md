# Wordpress Site Builder Applicant 
This repository provides a development environment for Wordpress Site Builders to complete example development tasks.

## Requirements
You will need to install the following programs onto your computer:
* [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)

## Usage
Once you have installed Virtualbox and Vagrant, clone this repository to your computer. Then, in your terminal, run the following command from the location you cloned the repository:

```
vagrant up
```

You should see some output like this:

```
Bringing machine 'default' up with 'virtualbox' provider...
==> default: Importing base box 'drud/applicantbox'...
==> default: Matching MAC address for NAT networking...
==> default: Checking if box 'drud/applicantbox' is up to date...
==> default: Setting the name of the VM: applicantbox_default_1464983823828_76115
==> default: Clearing any previously set network interfaces...
==> default: Preparing network interfaces based on configuration...
    default: Adapter 1: nat
==> default: Forwarding ports...
    default: 80 (guest) => 1025 (host) (adapter 1)
    default: 22 (guest) => 2222 (host) (adapter 1)
==> default: Running 'pre-boot' VM customizations...
==> default: Booting VM...
==> default: Waiting for machine to boot. This may take a few minutes...
    default: SSH address: 127.0.0.1:2222
    default: SSH username: vagrant
    default: SSH auth method: private key
    default:
    default: Vagrant insecure key detected. Vagrant will automatically replace
    default: this with a newly generated keypair for better security.
    default:
    default: Inserting generated public key within guest...
    default: Removing insecure key from the guest if it's present...
    default: Key inserted! Disconnecting and reconnecting using new SSH key...
==> default: Machine booted and ready!
==> default: Checking for guest additions in VM...
==> default: Mounting shared folders...
    default: /var/www => /Users/tannerjfco/devops/applicantbox
==> default: Running provisioner: shell...
    default: Running: /var/folders/n4/40fxh9_563qgh2z7qmtw2rg00000gn/T/vagrant-shell20160603-13990-116pyvl
==> default: stdin: is not a tty
==> default: Starting up the development environment...
==> default: # github.com SSH-2.0-libssh-0.7.0
==> default: # github.com SSH-2.0-libssh-0.7.0
==> default: no hostkey alg
==> default: The development environment is ready! You can now access the website in your browser at http://localhost:1025
==> default: The website codebase is in the folder 'applicantdemowp'
```

Once this has completed, you are ready to start your development tasks.

## Accessing the demo site
You can now access the site at http://localhost:1025

To log into the Wordpress Admin, go to http://localhost:1025/wp/wp-login.php and login with the following credentials:

*Username:* nmd.admin
*Password:* admin

## When your tasks are completed
Once you are done with your tasks, run the following command:
```
vagrant suspend
```
This will save the state of the site. You can then bring your computer to the follow-up interview to demonstrate the work.

## Removing this from your system
*DO NOT DO THIS UNTIL WE HAVE REVIEWED YOUR WORK!*
Once you have completed your development tasks and submitted them with a Pull Request, you can destroy the environment:

```
vagrant destroy
```

You can then remove the environment from your system:

```
vagrant box remove drud/applicantbox
```

Once this is completed, you can remove this repository from your computer.
