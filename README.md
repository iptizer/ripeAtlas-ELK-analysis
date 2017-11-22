# Overview

With this repository you can take a look at some data provided by the [ripe atlas](https://atlas.ripe.net/) project using the ELK-Stack. Simply execute the 5 commands from the Quickstart chapter and you'll be able to analyse some data within minutes.


Prerequisits, locally installed:

* ansible
* vagrant
* virtual box

Warning:

* By default the create virtual machine takes 8G of RAM and 4 cores
* By default the virtual machine takes up 40G disk space

# Quickstart

Enter the following commands in your terminal. After a few minutes a browser should pop up with kibana running.

```
git clone https://github.com/iptizer/ripeAtlas-ELK-analysis.git
cd ripeAtlas-ELK-analysis
vagrant up
ansible-galaxy install -r roles/requirements.yml
ansible-playbook site.yml
open http://admin:admin@localhost:8080/
```

Add ```logstash-*``` as index in Kibana es explained in [this playbooks README chapter.](https://github.com/sadsfae/ansible-elk#elkefk-server-instructions)

# Tipps

## Elasticsearch

Delete whole index

``` 
curl -XDELETE 'localhost:9200/logstash-\*?pretty'
```
