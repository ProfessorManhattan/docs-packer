## Overview

This repository contains the source code used to automatically build minimal {{ variables.description }} VM images. The build process closely imitates the same process used by [chef/bento](https://github.com/chef/bento). In fact, you will see that most of the `scripts/` folder is symlinked to a chef/bento submodule.

This repository automates most of the process of keeping our {{ variables.description }} VM images up-to-date with the latest upstream source by:

* Using the vagrant-cloud post-processor to automatically upload the box after it is built
* Automating the retrieval of the source ISO file and checksum file by using another project of ours called [LatestOS](https://pypi.org/project/latestos/)

### Supported Virtualization Platforms

Most of our repositories support creating boxes for the following virtualization platforms:

* KVM
* Hyper-V
* Parallels
* VirtualBox
* VMWare

You can check out exactly what platforms this repository supports by browsing through the types in the `"builders"` section of the `template.json` file found in the root of this repository.
