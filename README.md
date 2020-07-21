# Ceph-deploy fix for octopus on python > 3.8

For users having an error while initial ceph deploy:
[ceph_deploy][ERROR ] RuntimeError: AttributeError: module 'platform' has no attribute 'linux_distribution'

## Reasoning

Method linux_distribution has been removed from python 3.8, this remotes.py uses parse_os_release method for OS identification

## Usage

Replace /usr/lib/python3/dist-packages/ceph_deploy/hosts/remotes.py with file provided.

