dockerd-ansible
===============

Role to install and configure Docker daemon

Requirements
------------

- Debian >= 9
- Ubuntu >= 18.04
- Users sepcified in variable `docker_user_list` must be already created in the OS

Role Variables
--------------

- `APT_ARCH`: System architecture in the format understood by debian/apt [Default: amd64]
- `APT_RELEASE_CHANNEL`: Docker release channel (stable/edge/nightly) [Default: stable]
- `DOCKER_APT_GPG_KEY_URL`: Debian GPG key url for docker [Default: https://download.docker.com/linux/ubuntu/gpg]
- `DOCKER_YUM_GPG_KEY_URL`: Centos/RHEL GPG key url for docker: [https://download.docker.com/linux/centos/gpg]
- `docker_user_list`: List of users to be added to the os group `docker`

Dependencies
------------

- A Debian or RHEL based system

Example Playbook
----------------

```yaml
    ---
    - hosts: localhost
      name: Install docker daemon
      become: true
      connection: local
      roles:
        - amritanshu_pandey.dockerd_ansible
```

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
