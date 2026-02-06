---
title: "Stop the services"
date: 2022-07-11T18:42:35+09:00
weight: 10
pre: "<b>A. </b>"
draft: false
---

##### 1. Stop The Services
###### 1) For Old nodes
{{< highlight html >}}
$ sudo systemctl stop kcnd
$ sudo systemctl stop telegraf
$ sudo systemctl stop datadog-agent
{{< /highlight >}}
{{< line_break >}}

###### 2) For New Nodes
{{< highlight html >}}
$ sudo systemctl stop kcnd
$ sudo systemctl stop telegraf
{{< /highlight >}}
{{< line_break >}}

{{< line_break >}}
{{< line_break >}}

If you finish this step, please click the next button ```>``` on the right side of this page.