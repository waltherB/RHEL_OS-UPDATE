Role Name
=========

1) Patch the TEST systems
2) Check if there is no side effects
3) Wait few days or weeks
4) Patch the PROD systems with the exact same patches that the TEST system has




Example Playbook
----------------

---
- name: Patch TEST or PROD servers
  hosts: all
  become: true
  gather_facts: true
 
  roles:
    - rhel_os-update

Example Playbook run
--------------------

ansible-playbook -i inventories/hosts patch-os.yml -e env_patch=test


License
-------

BSD


