---
title: "Replace nodekey and bls-nodekey"
date: 2022-07-11T18:42:35+09:00
weight: 50
pre: "<b>E. </b>"
draft: false
---

{{< line_break >}}
##### This Task should work with Kaia Foundation.
##### Please starr this task after Kaia Foundation remove tour CN from the Validator.

##### 5. Start Services
###### 1) CN 
{{< highlight html >}}
$ sudo systemctl start kcnd
$ sudo systemctl start telegraf
{{< /highlight >}}
{{< line_break >}}

###### 2) PN
{{< highlight html >}}
$ sudo systemctl start kpnd
$ sudo systemctl start telegraf
{{< /highlight >}}

{{< line_break >}}
{{< line_break >}}

If you finish this step, please click the next button ```>``` on the right side of this page.
