Role Name
=========
This role install MongoDB Across a Raspberry Pi cluster and initializes a Replica Set.

Requirements
------------
`ansible-galaxy collection install community.mongodb`

Role Variables
--------------
`mongodb_version`: The version of MongoDB to install

Dependencies
------------
`pip install pymongo`

Example Playbook
----------------

    - name: Install MongoDB Cluster
      hosts: all
      gather_facts: yes
      become: yes

      roles:
        - { role: mongodb, vars: { mongodb_version: "6.0" }, tags: [] }

License
-------

BSD

Author Information
------------------
Cameron Rosier <rosiercam@gmail.com>
