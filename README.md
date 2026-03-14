[![CI](https://github.com/de-it-krachten/ansible-role-apt_mirror/workflows/CI/badge.svg?event=push)](https://github.com/de-it-krachten/ansible-role-apt_mirror/actions?query=workflow%3ACI)


# ansible-role-apt_mirror

APT mirror setup for Ubuntu



## Dependencies

#### Roles
None

#### Collections
None

## Platforms

Supported platforms

- Ubuntu 20.04 LTS
- Ubuntu 22.04 LTS
- Ubuntu 24.04 LTS

Note:
<sup>1</sup> : no automated testing is performed on these platforms


## Role Variables
### defaults/main.yml
<pre><code>
# Location where you want to store the mirrored files
apt_mirror_path: /data/install/ubuntu

# APT packages to install
apt_mirror_packages:
  - apt-mirror

# Ubuntu releases to mirror
apt_mirror_releases:
  # - focal
  - jammy
  # - noble

# Schedule mirror job
apt_mirror_schedule: false
</pre></code>




## Example Playbook
### molecule/default/converge.yml
<pre><code>
- name: sample playbook for role 'apt_mirror'
  hosts: all
  become: 'yes'
  tasks:
    - name: Include role 'apt_mirror'
      ansible.builtin.include_role:
        name: apt_mirror
</pre></code>
