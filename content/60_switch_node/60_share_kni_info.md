---
title: "Share the KNI Value for Node Information"
date: 2022-07-11T18:42:35+09:00
weight: 30
pre: "<b>C. </b>"
draft: false
---

{{< line_break >}}
##### This Task should work with Kaia Foundation.
##### Please starr this task after Kaia Foundation remove tour CN from the Validator.

##### 1. Start Services
###### 1) CN 
{{< highlight html >}}
$ sudo kcn attach --exec "admin.nodeInfo.kni" --datadir DATA_DIR
{{< /highlight >}}
{{< line_break >}}

###### 2) PN
{{< highlight html >}}
$ sudo kpn attach --exec "admin.nodeInfo.kni" --datadir DATA_DIR
{{< /highlight >}}

##### 2. Compare KNI value with your backup and Share it to the Slack channel.
{{< line_break >}}

{{< line_break >}}
{{< line_break >}}
{{< line_break >}}

If you finish this step, please click the next button ```>``` on the right side of this page.
