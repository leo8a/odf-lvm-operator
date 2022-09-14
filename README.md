# Ansible Role: ODF LVM operator

[![CI](https://github.com/leo8a/odf-lvm-operator/actions/workflows/ci.yml/badge.svg)](https://github.com/leo8a/odf-lvm-operator/actions/workflows/ci.yml)

Installs the [ODF LVM](https://github.com/red-hat-storage/lvm-operator.git) operator on OpenShift clusters.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    catalog_source: "redhat-operators"
    lvm_operator_namespace: "openshift-storage"
    lvm_operator_channel: "stable-4.10"

## Dependencies

This role requires the `kubernetes.core` collection, and have been tested on an OpenShift cluster version 4.10.

## Example Playbook

    - hosts: localhost
      gather_facts: false
      roles:
        - leo8a.odf_lvm_operator

For disconnected environments, the `catalog_source` var can be adjusted as follows:

    - hosts: localhost
      gather_facts: false
      roles:
        - leo8a.odf_lvm_operator
      vars:
        - catalog_source: "redhat-operator-index"

## License

This role is released under the Apache 2.0 license. See the [LICENSE](LICENSE).

## Author Information

This role was created in 2022 by [Leo Ochoa](https://github.com/leo8a/).

## Contributors

This is the current list of folks in the `odf_lvm_operator` hall of ~~fame~~ contributors 🏆!

<a href="https://github.com/leo8a/odf-lvm-operator/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=leo8a/odf-lvm-operator"  alt=""/>
</a>

> Made with [contributors-img](https://contrib.rocks).
