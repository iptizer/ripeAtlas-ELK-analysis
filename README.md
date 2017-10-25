# Overview

With this repository you can take a look at some data provided by the [ripe atlas](https://atlas.ripe.net/) project using the ELK-Stack. Simply execute the 5 commands from the Quickstart chapter and you'll be able to analyse some data within minutes.


Prerequisits, locally installed:

* ansible
* vagrant
* virtual box

Warning:

* By default the create virtual machine takes 12G of RAM and 4 cores
* By default the virtual machine takes up 40G
* By default a ~1.2G file will be downloaded while running

# Quickstart

```
git clone https://github.com/iptizer/ripeAtlas-ELK-analysis.git
cd ripeAtlas-ELK-analysis
vagrant up
ansible-galaxy install -r roles/requirements.yml
ansible-playbook site.yml
```
