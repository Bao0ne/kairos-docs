---
title: "Kairos release v2.2"
date: 2023-06-15
linkTitle: "Announcing v2.2 Kairos release"
description: "Kairos 2.2 release: ARM enhancements"
author: Ettore Di Giacinto ([X](https://x.com/mudler_it)) ([GitHub](https://github.com/mudler))
---
<h1 align="center">
  <br>
     <img width="184" alt="kairos-white-column 5bc2fe34" src="https://user-images.githubusercontent.com/2420543/215073247-96988fd1-7fcf-4877-a28d-7c5802db43ab.png">
    <br>
<br>
</h1>

Kairos is a cloud-native meta-Linux distribution that brings the power of public cloud to your on-premises environment. With Kairos, you can build your own cloud with complete control and no vendor lock-in. It allows you to easily spin up a Kubernetes cluster with the Linux distribution of your choice, and manage the entire cluster lifecycle with Kubernetes.

#### Why you should try Kairos:
Kairos provides a wide range of use cases, from Kubernetes applications to appliances and more. You can provision nodes with your own image or use Kairos releases for added flexibility. Kairos also simplifies day-2 operations like node upgrades. It provides the benefits of a unified, cloud-native approach to OS management.

#### What you can do with Kairos:
With Kairos, you can create an immutable infrastructure that stays consistent and free of drift with atomic upgrades. You can manage your cluster's entire lifecycle with Kubernetes, from building to upgrading. Kairos also allows you to automatically create multi-node, single clusters that span across regions for maximum flexibility and scalability.

## Kairos 2.2.0 release

Kairos 2.2.0 has just been released, and we are thrilled to share the latest updates and improvements to the Kairos project. This release is a major release as reflect changes to internal core components and enhanced support for the ARM architecture.
  
### What changed?

This release brings updates to the Kairos core components, including a substantial refactor of internal components and several bugfixes.

In order to enhance the user experience and reduce maintenance efforts the `elemental` cli and the `kairos-agent` functionalities were merged together. The `kairos-agent` now is responsible for the lifecycle of Kairos. This includes upgrades, setup, and delegating configuration to the specific providers that implement the specific configuration (k3s, for instance). The cloud-init stages can be run directly with the `kairos-agent`, and there is a `--debug` flag now to ease out troubleshooting. We also have renamed and moved user-facing commands of the Kairos CLI to `kairosctl`.

Besides, the Kairos agent now is capable to support multi-arch images, as such is now possible to specify container images during upgrades for different platforms within the same tag.

We consolidated our support for the ARM architecture, most notably:

- Generic iso ARM images, that can be used for development or in VMs
- Support for [Nvidia AGX Orin](https://kairos.io/docs/installation/nvidia_agx_orin/)!
- RPI images now are shipping with LVM, and as such the oem partition is available as in the `x86_64` flavors. Note: Reset is not working, we are addressing this into a patch release.
- Add ubuntu to the available RPI images

We are working also on a pure, Alpine flavor, which is now independent from systemd. Stay tuned!

If you are curious on what's next, check out our [Roadmap](https://github.com/orgs/kairos-io/projects/2) and feel free to engage with our [community](https://kairos.io/community/)!

---

For a full list of changes, see the  [Changelog](https://github.com/kairos-io/kairos/releases/tag/v2.2.0). We hope you find these updates useful and as always, let us know if you have any questions or feedback. Thanks for using Kairos!
