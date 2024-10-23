---
title: "Kairos release v3.1"
date: 2024-07-11
linkTitle: "Kairos release v3.1"
description: "Kairos release v3.1"
author: Mauro Morales ([X](https://x.com/mauromrls)) ([GitHub](https://github.com/mauromorales))
---
<h1 align="center">
  <br>
     <img width="184" alt="kairos-white-column 5bc2fe34" src="https://user-images.githubusercontent.com/2420543/215073247-96988fd1-7fcf-4877-a28d-7c5802db43ab.png">
    <br>
<br>
</h1>

We are thrilled to announce the release of Kairos v3.1.0! This update brings a host of significant enhancements to further secure and streamline your edge computing environment.

## Key Features and Updates

## Unified Kernel Images (UKI)
- Measured systemd-sysext: Introducing the ability to measure systemd extensions, enhancing security and integrity.
- Verify Upgrade Artifacts Signature: Ensuring the authenticity of upgrade EFI files before applying updates.
- Autoenroll Keys: Automatically enroll keys during live CD boot in setup mode for seamless initialization.
- Slim Artifacts to address memory constrains on some devices.

## Base Distribution Updates

- Updated support for Fedora 40, Ubuntu 24.04, and Leap 15.6, ensuring compatibility with the latest releases.

## Expanded Support

- Debian on ARM: Now supporting ARM architecture for Debian, broadening the hardware compatibility.
- HTTPS Support for IPXE Artifacts: Enhancing security with HTTPS support for IPXE artifacts.

## Potential Breaking Changes

By default, UKI artifacts now exclude Linux modules and firmware to reduce file
size for better EFI compatibility. This may impact hardware support. Review the
full changelog on GitHub for details on how to customize these artifacts to
meet specific hardware needs. Read more about this on the [release notes](/v3.1.0/docs/).

## Full Changelog

For a detailed list of changes, improvements, and known issues, please visit the [full changelog on GitHub](https://github.com/kairos-io/kairos/releases/tag/v3.1.0).

This release is a testament to our commitment to providing a robust and secure
edge computing platform. We extend our deepest gratitude to our community for
their invaluable contributions and support.

Thank you for being a part of the Kairos journey. Happy upgrading!

Stay tuned for more updates and enhancements.
