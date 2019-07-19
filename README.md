# yggdrasil-munin-plugin
[Munin monitoring](http://munin-monitoring.org/) plugin for [yggdrasil mesh network server](https://yggdrasil-network.github.io/)

## Files
Config file example: etc/munin/plugin-conf.d/yggdrasil

Plugin (PERL script): usr/share/munin/plugins/yggdrasil_

## Install

* Copy config file into /etc/munin/plugin-conf.d and plugin script into /usr/share/munin/plugins/ or /usr/local/share/munin/plugins/ 
* Link plugin script to /etc/munin/plugins/yggdrasil_traffic and /etc/munin/plugins/yggdrasil_connections.
* Check plugins by command `sudo munin-run -d yggdrasil_traffic` and `sudo munin-run -d yggdrasil_connections`. You must see something like

`awdl_recv.value 0`

`awdl_sent.value 0`

`self_recv.value 711369192`

`self_sent.value 589515156`

`tcp_recv.value 197478832`

`tcp_sent.value 181532597`

`total_recv.value 908848024`

`total_sent.value 771047753`

for traffic and

`n_connect_awdl.value 0`

`n_connect_self.value 1`

`n_connect_sim.value 0`

`n_connect_tcp.value 2`

`n_connects.value 3` 

for connections plugin.
* Restart munin-node.
* Enjoy.




