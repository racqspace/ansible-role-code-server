# Ansible Role: code_server

![MIT](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)
![GitHub Workflow Status](https://img.shields.io/github/workflow/status/racqspace/ansible-role-code-server/Main?style=flat-square)
![GitHub last commit](https://img.shields.io/github/last-commit/racqspace/ansible-role-code-server?style=flat-square)
![GitHub Release Date](https://img.shields.io/github/release-date/racqspace/ansible-role-code-server?style=flat-square)
![Maintenance](https://img.shields.io/maintenance/yes/2022?style=flat-square)

![Ansible Role](https://img.shields.io/ansible/role/56296?style=flat-square)
![Ansible Quality Score](https://img.shields.io/ansible/quality/56296?style=flat-square)

Install and setup [code-server](https://github.com/cdr/code-server).

## Highlights
* Run Visual Studio Code on any machine anywhere and access it in the browser
* Code on any device with a consistent development environment
* Use cloud servers to speed up tests, compilations, downloads, and more
* Preserve battery life when you're on the go; all intensive tasks run on your server

More information about code-server at: https://github.com/cdr/code-server

## Role Variables

Variable Name | Default Value | Description
------------ | ------------- | -------------
code_server_cache_valid_time | 3600 | Cache update time for apt module.
code_server_user | "{{ lookup('env', 'USER') }}" | User running code-server.
code_server_bind_addr | 127.0.0.1:8080 | Bind Address for code-server.
code_server_password | plaintextPassword | INSECURE WAY to set the password.
code_server_hashed_password |  | PREFERED WAY to set the password. learn how to use it at https://coder.com/docs/code-server/v3.12.0/FAQ#can-i-store-my-password-hashed

## Role Usage Examples

Example for installing code-server with "myPassword" as plaintext password.

```yaml
- hosts: all
  roles:
  - role: racqspace.code_server
    vars:
      code_server_password: myPassword
```

## License

MIT

## Author Information

This role was created in 2021 by [Clemens Kaserer](https://www.ckaserer.dev/).

Contributions by:

- [@ckaserer](https://github.com/ckaserer)
