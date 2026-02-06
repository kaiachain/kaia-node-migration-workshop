---
title: "Resource List of Backup"
date: 2022-07-11T19:18:57+09:00
weight: 20
pre: "<b>B. </b>"
draft: false
---

{{< line_break >}}

##### 1. Backup List of the CN

###### 1) kcnd.conf 
{{< highlight html >}}
sudo find / -name "kcnd.conf"
{{< /highlight >}}
###### 2) nodekey under DATA_DIR and bls-nodekey under DATA_DIR/klay
{{< highlight html >}}
sudo find / -name "kcnd.conf" -exec grep "DATA_DIR=" {} + | grep -v "#"
{{< /highlight >}}
###### 3) DataDog Configuration File
{{< highlight html >}}
/etc/datadog-agent/datadog.yaml
/etc/datadog-agent/conf.d/go.d/conf.yaml
{{< /highlight >}}
###### 4) Telegraf configuration File
{{< highlight html >}}
/etc/telegraf/telegraf.d/klaytn.conf
OR
/etc/telegraf/telegraf.d/kaia.conf
{{< /highlight >}}
###### 5) Note KNI Value 
{{< highlight html >}}
sudo kcn attach --exec "admin.nodeInfo.kni" --datadir DATA_DIR
"kni://abcdefg@[::]:32323?ntype=cn"
{{< /highlight >}}
{{< line_break >}}
{{< highlight html >}}
change @[::] part to @Your_public_IP_address
{{< /highlight >}}

{{< line_break >}}

##### 2. Backup List of the PN

###### 1) kpnd.conf 
{{< highlight html >}}
sudo find / -name "kpnd.conf"
{{< /highlight >}}
###### 2) nodekey under DATA_DIR and bls-nodekey under DATA_DIR/klay
{{< highlight html >}}
sudo find / -name "kpnd.conf" -exec grep "DATA_DIR=" {} + | grep -v "#"
{{< /highlight >}}
###### 3) DataDog Configuration File
{{< highlight html >}}
/etc/datadog-agent/datadog.yaml
/etc/datadog-agent/conf.d/go.d/conf.yaml
{{< /highlight >}}
###### 4) Telegraf configuration File
{{< highlight html >}}
/etc/telegraf/telegraf.d/klaytn.conf
OR
/etc/telegraf/telegraf.d/kaia.conf
{{< /highlight >}}
###### 5) Note KNI Value 
{{< highlight html >}}
sudo kpn attach --exec "admin.nodeInfo.kni" --datadir DATA_DIR
"kni://abcdefg@0.0.0.0:0"
{{< /highlight >}}
{{< line_break >}}
{{< highlight html >}}
change @0.0.0.0:0 part to @Your_public_IP_address:32323?ntype=pn
{{< /highlight >}}
###### 6) static-nodes.json 
{{< highlight html >}}
/Data_Dir/static-nodes.json
{{< /highlight >}}
{{< line_break >}}



{{< line_break >}}

{{< line_break >}}
If you finish this step, please click the next button ```>``` on the right side of this page.