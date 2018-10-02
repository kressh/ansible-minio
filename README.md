# Minio role for ansible

Create `./library` directory in your ansible project:

```
mkdir ./library
```

And configure `ansible.cfg`:

```
[defaults]
roles_path = ./library
```

Add submodule:

```
git submodule add git@github.com:kressh/ansible-minio.git library/minio
```

Use role:

```yaml
---
- hosts: cdn01.yourserver.io
  remote_user: ansible
  become: true
  roles:
    - minio
```

See default variables at `defaults/main.yml`.
