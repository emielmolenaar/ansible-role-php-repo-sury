Ondřej Surý's PHP packages repository role for Ansible
=================

A simple role for adding the [Ondřej Surý PHP repository](https://deb.sury.org/) on your APT-enabled hosts using [Ansible](http://www.ansibleworks.com/).

Usage
-----

This role uses [APT](https://docs.ansible.com/ansible/latest/modules/apt_module.html) to ensure the repository is added on your hosts. You might checkout Jeff Geerling's [PHP Role](https://github.com/geerlingguy/ansible-role-php) for actually installing and configuring PHP on your hosts.

Clone this repo into your roles directory:

    $ git clone https://github.com/emielmolenaar/ansible-role-php-repo-sury.git roles/php-repo-sury

And add it to your play's roles:

    - hosts: ...
      roles:
        - php-repo-sury
        - ...

I recommend using a `requirements.yml` in your roles directory though:

    - src: https://github.com/emielmolenaar/ansible-role-php-repo-sury.git
      name: php-repo-sury

Installing the role will require a `ansible-galaxy install -r ./roles/requirements.yml -p ./roles` from the root directory of your playbook.

Thanks
---

Thanks to the efforts of [Ondřej Surý](https://twitter.com/oerdnj) and [Jeff Geerling](https://www.jeffgeerling.com/), life is so much easier!
