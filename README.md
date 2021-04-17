Operator SDK
=========

Installs the [Operator-SDK](https://sdk.operatorframework.io/)

Requirements
------------

Import the Operator SDK's release keys

```shell
gpg --receive-keys 8613DB87A5BA825EF3FD0EBE2A859D08BF9886DB
```

Role Variables
--------------

| Name                      | Description                      | Default Value |
|---------------------------|----------------------------------|---
| operator_sdk_version      | Version to install               | 1.6.1
| operator_sdk_download_dir | Directory to download files to   | $HOME/tools/operator-sdk-$operator_sdk_version
| operator_sdk_install_dir  | Directory to install binaries in | $HOME/bin

Example Playbook
----------------

```yaml
- hosts: localhost
  roles:
    - role: ricfeatherstone.operator-sdk
      operator_sdk_version: 1.6.1
      operator_sdk_download_dir: /tools
      operator_sdk_install_dir: /usr/local/bin
```

License
-------

Apache 2.0 license. See the [LICENSE](LICENSE) file for details.
