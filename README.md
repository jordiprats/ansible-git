# Role Name

Install git and clone repositories to the system

## Role Variables

### git_repositories

* repo: repo URL to clone
* path: absolute path on the system to clone it 
* version: optional, clone a specific tag (default: HEAD)

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
---
- name: base
  hosts: all
  become: yes
  gather_facts: yes

  roles:
    - role: git

  vars:
    git_repositories:
     - repo: https://github.com/jordiprats/puppet-masterless
       path: /opt/masterless_version
       version: 0.1.0
     - repo: https://github.com/jordiprats/puppet-masterless
       path: /opt/masterless_head
```

## License

Apache-2.0
