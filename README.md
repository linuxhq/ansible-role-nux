# ansible-role-nux

[![Build Status](https://travis-ci.org/linuxhq/ansible-role-nux.svg?branch=master)](https://travis-ci.org/linuxhq/ansible-role-nux)
[![Ansible Galaxy](https://img.shields.io/badge/ansible--galaxy-nux-blue.svg?style=flat)](https://galaxy.ansible.com/linuxhq/nux)
[![License](https://img.shields.io/badge/license-GPLv3-brightgreen.svg?style=flat)](COPYING)

RHEL/CentOS - Nux repository

## Requirements

This role requires that you have the epel repository installed.

 * https://galaxy.ansible.com/linuxhq/epel/

## Role Variables

Available variables are listed below, along with default values:

    nux_arch: "{{ ansible_architecture }}"
    nux_dist: "{{ ansible_distribution_major_version }}"
    nux_baseurl: "http://li.nux.ro/download/nux/dextop/el{{ nux_dist }}/{{ nux_arch }}"
    nux_package: nux-dextop-release
    nux_disablerepo: []
    nux_enablerepo: []
    nux_packages: []
    nux_repository_nux_dextop: false
    nux_repository_nux_dextop_testing: false

## Dependencies

None

## Example Playbook

    - hosts: servers
      roles:
        - role: linuxhq.nux
          nux_enablerepo:
            - epel
          nux_packages:
            - ffmpeg
          nux_repository_nux_dextop: true

## License

Copyright (C) 2018 Taylor Kimball <tkimball@linuxhq.org>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <http://www.gnu.org/licenses/>.
