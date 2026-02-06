---
title: "Replace nodekey and bls-nodekey"
date: 2022-07-11T18:42:35+09:00
weight: 20
pre: "<b>B. </b>"
draft: false
---

##### 2. Remove Temporary nodekey and bls-nodekey on New Node
###### 1) For CN 
{{< highlight html >}}
$ mv /<Data_DIR>/klay/nodekey /<Data_DIR>/data/klay/nodekey_temp
$ mv /<Data_DIR>/klay/bls-nodekey /<Data_DIR>/data/klay/bls-nodekey_temp
$ sudo vi /<Data_DIR>/nodekey # Paste the Nodekey what you made
{{< /highlight >}}
{{< line_break >}}

###### 2) For PN 
{{< highlight html >}}
$ mv /<Data_DIR>/klay/nodekey /<Data_DIR>/data/klay/nodekey_temp
$ mv /<Data_DIR>/klay/bls-nodekey /<Data_DIR>/data/klay/bls-nodekey_temp
$ sudo vi /<Data_DIR>/nodekey # Paste the Nodekey what you made
{{< /highlight >}}

{{< line_break >}}
{{< line_break >}}

If you finish this step, please click the next button ```>``` on the right side of this page.