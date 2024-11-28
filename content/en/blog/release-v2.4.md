---
title: "Kairos release v2.4"
date: 2023-09-19
linkTitle: "Kairos release v2.4"
description: "Kairos release v2.4"
author: Dimitris Karakasilis ([LinkedIn](https://www.linkedin.com/in/dkarakasilis/)) ([GitHub](https://github.com/jimmykarily))
---
<h1 align="center">
  <br>
     <img width="184" alt="kairos-white-column 5bc2fe34" src="https://user-images.githubusercontent.com/2420543/215073247-96988fd1-7fcf-4877-a28d-7c5802db43ab.png">
    <br>
<br>
</h1>

We're thrilled to announce the release of version 2.4.0 of Kairos which brings a wealth of exciting improvements and essential bug fixes that we can't wait to share with you.

## Enhanced Release Artifacts Naming

One of the significant changes in this release is the revamp of our release artifacts naming. We've worked hard to make them more consistent and easier to identify, streamlining your experience in finding the right elements for your project.

## Raspberry Pi Enhancements

For those using Raspberry Pi devices, we've addressed several issues, including serial console problems and auto expansion of the last partition, among others. This ensures a smoother experience when using our project on Raspberry Pi devices, making it more versatile and reliable than ever before. We've also split the RPI images into rpi3 and rpi4 versions due to partitioning issues, with support for GPT being exclusive to rpi4.

## Configuration Centralization

We've taken a step toward simplifying your configuration process by consolidating all settings to the kairos-config (/etc/elemental/config.yaml is no longer used). This change streamlines your configuration management, making it more straightforward and efficient.

## Merged Release Pipelines

In an effort to provide a more unified experience, we've merged the kairos-io/kairos and kairos-io/provider-kairos release pipelines. Going forward, kairos-io/kairos will serve as the canonical location for all artifacts, both "standard" and "core," making it easier than ever to access and manage your resources.

## K3S Releases Alignment

To align more closely with upstream releases, we have limited the number of k3s releases bundled with our project to match the three most recent minor release versions. This ensures that you have access to the latest features and improvements while maintaining stability.

## Streamlined Package Management

Kairos overlay files now come directly from luet packages, eliminating the need for them to be included in the repository. Similarly, K3S packages are now sourced directly from luet packages, providing better control over versions and ensuring a more consistent upgrade cadence.

## Kairos Agent Updates (v2.2.11)

Our Kairos agent has received significant updates in this release, bringing a host of improvements and new features:

- Single Source for Configuration: We've simplified configuration management by merging two different files into one, the cloud-config, for configuring install, upgrade, and reset behaviors. Check out the full reference in our documentation to migrate your existing configurations.

- Create Dirs in Rootfs: For situations where you need to create directories in the rootfs, we've introduced a new option in the configuration to facilitate this process, enhancing flexibility.

- Upgrade Workflow from Passive: We've improved the upgrade workflow when booting from the passive image, ensuring that only the active image is updated, preventing issues with a broken system.

- Auto Partition and Image Size: Say goodbye to fixed partition and image sizes. The agent now dynamically calculates optimal sizes based on the source for installation, creating partitions accordingly.

- Overridable Partition and Image Size: If you prefer to customize partition and image sizes, you can now do so directly via cloud config, allowing you to fine-tune the sizes for each action (install, upgrade, reset).

- Improved Unattended Reset: Unattended reset now works seamlessly in any terminal or service, automatically rebooting when needed. It offers greater flexibility and reliability across various scenarios.

- run-stage Command: We've fixed several underlying issues related to cloud provider metadata, user creation, and partition layout, ensuring a smoother operation.

 - Upgrade Recovery: Recovery upgrades are now possible with the introduction of flags to facilitate the process. Normal upgrades also include a warning to remind users to upgrade recovery when necessary.


For a comprehensive view of all the changes in this release, please refer to [the full changelog](https://github.com/kairos-io/kairos/releases/tag/v2.4.0) (And be sure to check out the "Known issues" section for any potential hiccups.)

This release marks a significant milestone in the evolution of our project, and we want to extend our heartfelt thanks to everyone who contributed to this release. Whether through code contributions, reviews, bug reports, comments, debugging output, or simply joining [our meetings](https://calendar.google.com/calendar/u/0/embed?src=c_6d65f26502a5a67c9570bb4c16b622e38d609430bce6ce7fc1d8064f2df09c11@group.calendar.google.com&ctz=Europe/Rome), your support and engagement are invaluable.

Stay awesome, and keep the momentum going!
