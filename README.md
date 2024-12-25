# Tom's Go Ansible Role

An Ansible role to install and configure Go.

## Available Variables

| Variable          | Type     | Default  | Description |
|:------------------|:--------:|:--------:|:------------|
| go_install_method | string   | `repos`  | One of the following: `repos`, `binary`, or `source`. |
| go_version        | string   | `stable` | A semantic version number or keyword. If using a semantic version number, you must use one of the the following: just the major version (ie. `1`), the major-minor version (ie. `1.23`), or the major-minor-patch version (ie. `1.23.4`). Allowed keywords are: `latest`, `base`, or `stable`. |

#### Installing from Repos

##### RHEL and RHEL Derivatives

Go is made available through a rolling application stream, so its version
is updated throughout the lifecycle of Enterprise Linux. The following table
shows the rolling version when this _README_ was last updated.

| Enterprise Linux Version | Stream | Ruby Version |
|:------------------------:|:------:|:------------:|
| 9                        | `base` | 1.22.x       |

By default, `go_version` is set to `stable` which corresponds to the `base`
stream. There is no difference between `stable` and `latest`.

## Copyright &amp; License

Copyright © 2024 Tom "tdworz" Dworzanski.

This program is free software: you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation, either version 3 of the License, or (at your option) any later
version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A
PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with
this program. If not, see <https://www.gnu.org/licenses/>.
