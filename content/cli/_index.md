---
title: "Up CLI"
icon: "terminal"
weight: 200
description: "Install Crossplane, interact with the Upbound Marketplace and Managed Control Planes with the Upbound Up CLI."
---

The Upbound `up` command-line enables interaction with Upbound managed control planes. It also simplifies common workflows with Upbound Universal Crossplane (UXP) and building Crossplane packages for the Upbound Marketplace or any OCI-compliant registry.
<!-- vale Google.Headings = NO -->
## Install the Up command-line
<!-- vale Google.Headings = YES -->
Install the `up` command-line via shell, Homebrew or Linux package.

{{< tabs "up-install" >}}
{{<tab "Shell" >}}
Install the latest version of the `up` command-line via shell script by downloading the install script from [Upbound](https://cli.upbound.io).  

{{< hint "tip" >}}
Shell install is the preferred method for installing the `up` command-line.
{{< /hint >}}

The shell install script automatically determines the operating system and platform architecture an installs the correct binary. 

```shell
curl -sL "https://cli.upbound.io" | sh
```

{{< hint "note" >}}
Install a specific version of `up` by providing the version. 

For example, to install version `v0.12.1` use the following command:

```shell
curl -sL "https://cli.upbound.io" | VERSION=v0.12.1 sh
```

Find the full list of versions in the <a href="https://cli.upbound.io/stable?prefix=stable/">Up command-line repository</a>.
{{< /hint >}}

{{< /tab >}}

{{< tab "Homebrew" >}}
[Homebrew](https://brew.sh/) is a package manager for Linux and Mac OS.  

Install the `up` command-line with a Homebrew `tap` using the command:

```shell
brew install upbound/tap/up
```
{{< /tab >}}
{{< tab "LinuxPackages" >}}

Upbound provides both `.deb` and `.rpm` packages for Linux platforms.

Downloading packages requires both the [version](https://github.com/upbound/up/releases) and CPU architecture (`linux_amd64`, `linux_arm`, `linux_arm64`).

### Debian package install
```shell
curl -sLo up.deb "https://cli.upbound.io/stable/${VERSION}/deb/linux_${ARCH}/up.deb"
```
<br />

<!-- vale Microsoft.HeadingAcronyms = NO -->
### RPM package install
<!-- vale Microsoft.HeadingAcronyms = YES -->
```shell
curl -sLo up.rpm "https://cli.upbound.io/stable/${VERSION}/rpm/linux_${ARCH}/up.rpm"
```
{{< /tab >}}
{{< /tabs >}}
