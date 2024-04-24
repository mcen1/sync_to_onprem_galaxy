## sync_to_onprem_galaxy

This github repository contains a playbook with roles to download collections and upload them to an on-prem galaxy mirror.

## why use this instead of using the built-in synchronization functionality inside the galaxy instance?

When I tried that, the galaxy-worker (which I think runs or is based on the pulp worker) consumed so much memory it made my VM crash. I put in a resource limit of 4 Gi and it killed the container, making the synchronization fail. I'm reluctant to put a product like that onto anything important. This playbook is a more lightweight approach to solve my own use-case, which is to have a back-up in place if galaxy.ansible.com/api goes down again (which it had on April 5th 2024 https://forum.ansible.com/t/ansible-galaxy-not-functional/4757)
