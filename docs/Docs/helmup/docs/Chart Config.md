---
title: Chart Config
layout: default
parent: HelmUp
grand_parent: Docs
nav_order: 6.2
has_children: false
---
# sirrend.helm.cfg HelmUp Configuration File

The `sirrend.helm.cfg` file contains data about the chart located in the same directory as the file itself.  

**This file can be generated automatically by the HelmUp program or manually by the user.**

Our recommendation is to allow the system to identify the chart's characteristics on its own and to manually configure it only if a misconfiguration occurs.


```java
[chart]
name = keda
version = 2.11.0
kubeversion = >=v1.23.0-0
home = https://github.com/kedacore/keda
app_version = 2.11.0
classification = community
repository = https://kedacore.github.io/charts
values_file = /tmp/sirrend-kuba_test/keda/values.yaml
```

### Important Configurable Items:
* `classification` - Specifies the type of chart.  
It can be either `community` for community charts or `local` for self-written charts.

* `repository` - The Helm repository from which you can pull the chart.

### Important Unconfigurable Items:
* `values_file` - Refers to the location of the values file found in the cloned repository. This item is managed by the program and is not user-configurable.



