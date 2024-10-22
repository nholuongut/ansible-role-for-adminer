# Ansible Role: Adminer

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

An Ansible Role that installs [Adminer](http://www.adminer.org/) on almost any computer.

## Requirements

You need to have PHP and MySQL for Adminer to do anything useful. If you have Apache installed, Adminer will add in configuration to make Adminer accessible on any virtualhost at `/adminer`; set `adminer_add_apache_config` to `false` to disable this behavior.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    adminer_download_url: https://www.adminer.org/latest.php

The URL from which Adminer should be downloaded.

    adminer_install_dir: /opt/adminer

The directory in which Adminer will be downloaded/installed.

    adminer_install_filename: adminer.php

The filename for the downloaded Adminer application. If you're managing virtualhosts or server directives manually, it might be simpler to set the document root to your configured `adminer_install_dir`, and the filename to `index.php`, so you don't have to enter `/adminer.php` in the URL to access Adminer.

    adminer_symlink_dirs: []

Directories inside which you would like `adminer.php` symlinked. Can be useful if you just want to toss the script into a docroot and access it at `sitename/adminer.php`.

    adminer_add_apache_config: false

Set this to `true` to tell Adminer to add a config file to Apache so you can access it at `hostname/adminer` on any configured virtualhost, using an Apache `Alias` directive. The role will also restart Apache so this configuration takes effect immediately.

    adminer_theme: ''

You can use any theme from adminer library (for example `pappu687`). You can find the full list [here](https://www.adminer.org/en/#extras).

## Dependencies

None. If `adminer_add_apache_config` is set to `true`, it will use some variables and handlers defined by the `nholuong.apache` role, so there's a soft dependency on that role.

## Example Playbook

    - hosts: servers
      roles:
        - { role: nholuong.adminer }

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟
