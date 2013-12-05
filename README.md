Vagrant Ansible Drupal development
==================================

This includes the following technologies:

* MySQL
* Apache2
* PHP
* Varnish
* Git
* Drush (with the site audit module)
* Munin
* Xdebug
* SASS
* Sendmail
* Memcached
* Adminer
* XHProf

Prerequesites
-------------

* Vagrant (currently only VirtualBox tested)
* Ansible (with the Vagrant Ansible Pluigin)

To install Ansible use the following commands (tested on OSx):

    sudo easy_install pip
    sudo pip install ansible

Then install the Vagrant Ansible plugin

    vagrant plugin install ansible

Usage
-----

If you already have the needed elements then you can run it. To get up and running use the following:

    vagrant up

By adding the following rule to your hosts file you can view the sites test file using www.drupal.local
    
    192.168.100.100 www.drupal.local

To access the vagrant box use:

    vagrant ssh

To install Drupal on the box log in (using 'vagrant ssh') and run the script /var/www/drupal_install.sh. The admin username is 'admin' and the password is 'password'.

Once done use the following to throw everything away:

    vagrant destroy

Additional
----------

You can access MailCatcher via the following URL:
http://www.drupal.local:1080/

You can access Adminer via the following URL:
http://www.drupal.local/adminer/

You can access XHProf via the following URL:
http://www.drupal.local/xhprof/

Notices
-------

This box was originally developed by Phil Norton ([@philipnorton42](http://www.twitter.com/philipnorton42)) for use with the site [#! code](www.hashbangcode.com).

Thanks to [Mike Bell](http://mikebell.io/) for some of the Vagrant configuration settings.
Thanks to [Michael Heap](http://michaelheap.com/) for introducing me to Ansible.

All feedback very much appreciated :)