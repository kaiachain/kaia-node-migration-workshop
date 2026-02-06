---
title: "Node Configuration"
date: 2022-07-11T19:18:57+09:00
weight: 30
pre: "<b>C. </b>"
draft: false
---
{{< line_break >}}

### 1. Data, Log Directory Creation
Considering the fact that the size of Kaia blockchain data is always increased. &nbsp;

It is recommended to use a big enough storage. You may need to create the directory on your desired path.

{{< line_break >}}

###### 1) CN
{{< highlight html >}}
$ mkdir -p /var/kcnd/data
{{< /highlight >}}
{{< highlight html >}}
$ mkdir -p /var/kcnd/logs
{{< /highlight >}}

###### 2) PN
{{< highlight html >}}
$ mkdir -p /var/kpnd/data
{{< /highlight >}}
{{< highlight html >}}
$ mkdir -p /var/kpnd/logs
{{< /highlight >}}
{{< line_break >}}


{{< line_break >}}
{{< line_break >}}

### 4. Replace conf file - Restore file what you made in prerequisites
>Configuration File Location:
###### For the archive distribution, the config directory location defaults to `$INSTALL_PATH/kcn-linux-amd64/conf/`.
###### For the package distribution, the config directory defaults to `/etc/kcnd/conf/`.

{{< line_break >}}

---
{{< line_break >}}

*You can check the more information for installation on the page below.*
* CN : https://docs.kaia.io/docs/nodes/core-cell/install/install-consensus-nodes/
* PN : https://docs.kaia.io/docs/nodes/core-cell/install/install-proxy-nodes/

{{< line_break >}}
{{< line_break >}}
{{< line_break >}}

If you finish this step, please click the next button ```>``` on the right side of this page.

