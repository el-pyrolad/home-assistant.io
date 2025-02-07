---
title: Enphase Envoy
description: Instructions on how to setup Enphase Envoy with Home Assistant.
ha_category:
  - Energy
ha_release: 0.76
ha_iot_class: Local Polling
ha_domain: enphase_envoy
ha_zeroconf: true
ha_config_flow: true
ha_codeowners:
  - '@gtdiehl'
ha_platforms:
  - diagnostics
  - sensor
ha_integration_type: integration
---

A sensor platform for the [Enphase Envoy](https://enphase.com/en-us/products-and-services/envoy-and-combiner) solar energy gateway. Works with older models that only have production metrics (ie. Envoy-C) and newer models that offer both production and consumption metrics (ie. Envoy-S).

{% include integrations/config_flow.md %}

### Obtaining the password

For newer models, the username `envoy` without a password will grant access to the device. For older models, the password for the `installer` user can be obtained with this: [tool](https://thecomputerperson.wordpress.com/2016/08/28/reverse-engineering-the-enphase-installer-toolkit/).

In some cases, you need to use the username `envoy` with the last 6 digits of the unit's serial number as password. See [the enphase documentation](https://support.enphase.com/s/article/What-is-the-Username-and-Password-for-the-Administration-page-of-the-Envoy-local-interface) for more details on other units.
