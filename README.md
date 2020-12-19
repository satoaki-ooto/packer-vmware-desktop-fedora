# Vagrant Boxes - Fedora

## Overview

This repository contains Packer templates for creating Fedora Vagrant boxes.

## Current Boxes

- [Fedora 31](https://getfedora.org/ja/server/)
- [Fedora 32](https://getfedora.org/ja/server/)

## Building the Vagrant boxes with Packer

To build all the boxes, you will need installed requires the software listed below.  

- VMware
  - [Fusion](https://www.vmware.com/products/fusion)
  - [Workstation](https://www.vmware.com/products/workstation)

We make use of JSON files containing user variables to build specific version of Ubuntu.  
You tell `packer` to use a specific user variable file via the `-var-file=` command line option.  

For example, to build Fedora 31, use the following:  

```bash
# fedora 31 on VMware
$ FEDORA_VERSION=31 make build
```

For example, to build Fedora 32, use the following:  

```bash
# fedora 32 on VMware
$ FEDORA_VERSION=32 make build
```