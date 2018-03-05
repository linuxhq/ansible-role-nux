# ansible-role-nux

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-nux.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-nux)

RHEL/CentOS - Nux repository

## Requirements

None

## Role Variables

Available variables are listed below, along with default values:

    nux_arch: "{{ ansible_architecture }}"
    nux_dist: "{{ ansible_distribution_major_version }}"
    nux_baseurl: "http://li.nux.ro/download/nux/dextop/el{{ nux_dist }}/{{ nux_arch }}"
    nux_package: nux-desktop-release
    nux_disablerepo: []
    nux_enablerepo: []
    nux_packages: []
    nux_repository_nux_desktop: false
    nux_repository_nux_desktop_testing: false

## Dependencies

 * https://galaxy.ansible.com/linuxhq/epel/

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.nux
          nux_enablerepo:
            - epel
          nux_packages:
            - ffmpeg
          nux_repository_nux_desktop: true

## License

GPLv3

## Author Information

This role was created by [Taylor Kimball](http://www.linuxhq.org).
