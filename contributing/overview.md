## Overview

[chef/bento](https://github.com/chef/bento/tree/master/packer_templates) has already done most of the work we are trying to accomplish. They have Packer templates for everything except Archlinux and Mac OS X. Since it has a huge following, updates are likely to be provided. We will be using chef/bento as our upstream provider wherever possible. They provide shell scripts that do a lot of the setup we need to initialize boxes. In each of our repositories, we will include chef/bento as a submodule. By doing this, we will be able to symlink the shell scripts into our scripts folder. This repository serves as an example.

There are a few changes that need to be done. The first thing we will be doing is having one file named `template.json` in each OS family repository. Through automation, our vagrantup.com pages will (down the road) have the built boxes at all the different versions. This will be done automatically by using a project that another contractor made called [LatestOS](https://pypi.org/project/latestos/). The latest version of each Linux OS will be checked and compiled on a cron job on multiple machines so we can generate the assets for:

* Parallels
* Hyper-V
* KVM
* VirtualBox
* VMWare