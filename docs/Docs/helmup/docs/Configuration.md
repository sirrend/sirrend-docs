---
title: sirrend.cfg
layout: default
parent: helmup
grand_parent: Docs
nav_order: 6.1
has_children: false
---
# sirrend.cfg HelmUp Configuration File

The `sirrend.cfg` file contains all possible system configurations and features.

```java
[kubernetes]
current_kubernetes_version=1.24.10
desired_kubernetes_version=1.26.0

[general]
jira_tickets=enabled
teams_notifications=enabled
upgrade_majors=disabled
```

* `current_kubernetes_version` - the current Kubernetes version you have.
</br>
It is important for best upgrades compatability.

* `desired_kubernetes_version` - the Kubernetes version you whish to upgrade to (if any).
</br>
**It is not a must have value.**

* `jira_tickets` - Should Jira tickets be opened for each new Pull-Request or not. Defaults to `disabled`.

* `teams_notifications` - Should teams messages be sent or not.</br>
It is our recommendation to enable this feature, in order to receive all possible inputs regarding the upgrades and backend processes running daily.
</br>
Defaults to `disabled`.

* `upgrade_majors` - By design, HelmUp performs upgrades to the next minor version.  
When the last minor version is reached for the current major version, the program checks whether this value is `enabled`.  
If it is, `HelmUp` will attempt to proceed with the upgrade process to the next major version; otherwise, it will stop at the last patch version of the current major.

