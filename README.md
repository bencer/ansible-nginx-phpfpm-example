# ansible-nginx-phpfpm-example
Cookbook example of deploying Nginx and PHP-FPM with Ansible

This is a complete example of how to use Ansible (tested with 1.7.2) to
deploy Nginx and PHP-FPM.
Unlike most of the other tutorials, we are using existing modules from
Ansible Galaxy rather than building our own roles.
In addition we will be installing Server Density agent for monitoring.

## Prerequesites
Configure the hosts file with the IP address and username of the target server.

## Dependencies
We will be using some 3rd party modules:

* [jdauphant.nginx](https://github.com/jdauphant/ansible-role-nginx/)
* [debops.php5](https://github.com/debops/ansible-php5)
* [CorbanR/ansible-serverdensity](https://github.com/CorbanR/ansible-serverdensity/)

```
$ mkdir galaxy
$ ansible-galaxy install jdauphant.nginx
$ ansible-galaxy install debops.php5
$ git clone https://github.com/CorbanR/ansible-serverdensity && mkdir roles && ln -s ../ansible-serverdensity/roles/serverdensity .
```

## Contributions
Please fork and send your improvements via PRs.
