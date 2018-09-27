### Role to manage system users and groups

Found that we were re-writing this in our playbooks quite a bit, isn't quite a galaxy role yet


Metadata example
```yaml
system_groups:
  - group: foo
    gid: 1234
    state: present/absent #optional default present
  - group: bar
    gid: 4321

system_users:
  - name: sys-user
    uid: 2233
    group: sys-user
    groups: # Optional extra groups, will be merged with group above
    gid: 2233
    state: present/absent # optional default present
    profile: |
      #Contents of bash .profile file
```