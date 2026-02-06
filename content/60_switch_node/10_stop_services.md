---
title: "Check the services"
date: 2022-07-11T18:42:35+09:00
weight: 30
pre: "<b>C. </b>"
draft: false
---

{{< line_break >}}
##### 1. This Task should work with Kaia Foundation.

```Kaia Foundation remove from the Validator.``` 
```STOP services : k*nd, telegraf and Datadog-agent on Old Nodes and k*nd, telegraf on New Nodes.``` 
{{< highlight html >}}
$ sudo systemctl stop k*nd
$ sudo systemctl stop telegraf
$ sudo systemctl stop datadog-agent
{{< /highlight >}}
{{< line_break >}}
```change nodekey (DataDIR) and bls-nodekey (DataDir/klay) of CN``` 
{{< highlight html >}}
$ mv /<Data_DIR>/klay/nodekey /<Data_DIR>/data/klay/nodekey_temp
$ mv /<Data_DIR>/klay/bls-nodekey /<Data_DIR>/data/klay/bls-nodekey_temp
$ sudo vi /<Data_DIR>/nodekey # Paste the Nodekey what you made
{{< /highlight >}}
{{< line_break >}}
```change nodekey (DataDIR) and bls-nodekey (DataDir/klay) of PN``` 
{{< highlight html >}}
$ mv /<Data_DIR>/klay/nodekey /<Data_DIR>/data/klay/nodekey_temp
$ mv /<Data_DIR>/klay/bls-nodekey /<Data_DIR>/data/klay/bls-nodekey_temp
$ sudo vi /<Data_DIR>/nodekey # Paste the Nodekey what you made
{{< /highlight >}}
{{< line_break >}}
```Replace static-nodes.json of PN``` 
```change instance name and host name on /etc/telegraf/telegraf.d/kaia.conf from *-*n-new to *-*n ```
```start kcnd service of new node``` 

###### 1) For CN, Connect PN for Block Sync - Use KNI of what you made 
{{< highlight html >}}
$ sudo kcn attach --exec "admin.addPeer(PN KNI)" --datadir DATA_DIR
$ tail <your_kaia_home_path>/kcnd/log/kcnd.out
INFO Inserted a new block number=14 hash=13cbfc…f007fc txs=0 gas=0 elapsed=793.458µs processTxs=167ns finalize=157.708µs validateState=7.542µs totalWrite=443.417µs trieWrite=256.667µs
{{< /highlight >}}

###### 2) For PN, Connect PN for Block Sync - Use KNI of what you made
{{< highlight html >}}
$ sudo kpn attach --exec "admin.addPeer(PN KNI)" --datadir DATA_DIR
$ tail <your_kaia_home_path>/kcnd/log/kpnd.out
INFO Inserted a new block number=14 hash=13cbfc…f007fc txs=0 gas=0 elapsed=793.458µs processTxs=167ns finalize=157.708µs validateState=7.542µs totalWrite=443.417µs trieWrite=256.667µs
{{< /highlight >}}

{{< line_break >}}
If you finish this step, please click the next button ```>``` on the right side of this page.

###### 1) Rename auto-generated bls-key - will be deleted later
{{< highlight html >}}
$ mv /<Data_DIR>/klay/bls-nodekey /<your_kaia_home_path>/data/klay/bls-nodekey_temp
{{< /highlight >}}

{{< line_break >}}

###### 2) Create bls-nodekey file
{{< highlight html >}}
$ vi /<Data_DIR>/bls-nodekey
{{< /highlight >}}

#### Install from Kaia Yum Repo - We Recommend This



start kcnd service of new node - line
share the admin.nodeInfo.kni of the new CN  - line
restart kpnd service - line
Start telegraf service on new CN  - line
Add the Validator - kaia