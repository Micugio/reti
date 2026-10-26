cd /tmp  ->  comando per aprire la cartella temporanea Linux e lavorare lì, è una cartella in cui il contenuto viene cancellato ogni volta che riavvi il poc


COMANDI KATHARA SUL TERMINALE:

giovanni.giovannini@sci-b106pc064x:~$ docker --version
Docker version 29.1.3, build 29.1.3-0ubuntu3~24.04.2
giovanni.giovannini@sci-b106pc064x:~$ kathara --version
Current version: 3.8.0
giovanni.giovannini@sci-b106pc064x:~$ kathara vstart -n pc1
INFO     A new version of Kathara has been released.                            
INFO     Current: 3.8.0 - Latest: 3.8.3                                         
INFO     Please update it from https://github.com/KatharaFramework/Kathara      
┌──────────────────────────────────────────────────────────────────────────────┐
│                            Starting Device `pc1`                             │
└──────────────────────────────────────────────────────────────────────────────┘
INFO     Installing Kathara Network Plugin (kathara/katharanp_vde:amd64)...     
INFO     Kathara Network Plugin installed successfully!                         
INFO     Pulling image `kathara/base:latest`... This may take a while.          
[Download Complete 305616650ccc]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00
[Download Complete 9d2f29087bcd]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00
[Download Complete f21f289e2f5b]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00
[Download Complete 33c82049d30d]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00
[Download Complete 0224e64fdfab]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00
[Download Complete e79f9908ebdd]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00
[Download Complete cc81111e0bd3]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00
[Download Complete 5ce4262dd806]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00
[Download Complete 15f609155a80]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00
[Download Complete 8c96109d3205]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00
[Download Complete 4f4fb700ef54]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00
[Download Complete 7c22c7ac73c5]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00
[Download Complete 17bbfff4c4ea]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00
[Download Complete 638a7d3c87a3]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00
[Download Complete 3067451a1818]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 100% 0:00:00
[Deploying devices]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1/1
giovanni.giovannini@sci-b106pc064x:~$ kathara list
                                                                            TIMESTAMP: 2026-10-26 09:00:10.820600                                                                             
┌────────────────────────┬───────┬────────────────────────────────────────────┬─────────┬─────────────────────┬──────┬───────────┬────────────────────┬─────────────┬───────────┬────────────┐
│ NETWORK SCENARIO ID    │ NAME  │ USER                                       │ STATUS  │ IMAGE               │ PIDS │ CPU USAGE │ MEM USAGE          │ MEM PERCENT │ NET USAGE │ INTERFACES │
╞════════════════════════╪═══════╪════════════════════════════════════════════╪═════════╪═════════════════════╪══════╪═══════════╪════════════════════╪═════════════╪═══════════╪════════════╡
│ rMHnlcI87I74aEZKpwj7Q  │ pc1   │ giovannigiovannini-4fxdcpagmbbn9snjqih3yw  │ running │ kathara/base:latest │ 2    │ 0.00%     │ 1.77 MB / 15.29 GB │ 0.01 %      │ -         │ -          │
└────────────────────────┴───────┴────────────────────────────────────────────┴─────────┴─────────────────────┴──────┴───────────┴────────────────────┴─────────────┴───────────┴────────────┘
giovanni.giovannini@sci-b106pc064x:~$ kathara connect -v
usage: kathara connect [-h] [-d DIRECTORY | -v] [--shell SHELL] [-l] DEVICE_NAME
kathara connect: error: the following arguments are required: DEVICE_NAME
giovanni.giovannini@sci-b106pc064x:~$ kathara connect -v pc1
root@pc1:/# exit
exit


giovanni.giovannini@sci-b106pc064x:~$ kathara vclean -n pc1
┌────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                                                                   Stopping Device `pc1`                                                                                    │
└────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┘
[Deleting devices]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1/1


giovanni.giovannini@sci-b106pc064x:~/katharalab1$ kathara lstart
┌────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                                                                 Starting Network Scenario                                                                                  │
└────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┘
[Deploying collision domains]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1/1
[Deploying devices]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 2/2


giovanni.giovannini@sci-b106pc064x:~/katharalab1$ giovanni.giovannini@sci-b106pc064x:~/katharalab1$ kathara list
                                                                            TIMESTAMP: 2026-10-26 09:19:12.959359                                                                              
┌─────────────────────────┬───────┬───────────────────────────────────────────┬─────────┬─────────────────────┬──────┬───────────┬────────────────────┬─────────────┬───────────┬────────────┐ 
│ NETWORK SCENARIO ID     │ NAME  │ USER                                      │ STATUS  │ IMAGE               │ PIDS │ CPU USAGE │ MEM USAGE          │ MEM PERCENT │ NET USAGE │ INTERFACES │ 
╞═════════════════════════╪═══════╪═══════════════════════════════════════════╪═════════╪═════════════════════╪══════╪═══════════╪════════════════════╪═════════════╪═══════════╪════════════╡ 
│ A1HjyzSbDzYNYEgb5D7nDA  │ pc2   │ giovannigiovannini-4fxdcpagmbbn9snjqih3yw │ running │ kathara/base:latest │ 2    │ 0.00%     │ 1.71 MB / 15.29 GB │ 0.01 %      │ 0 B / 0 B │ 0:A        │ 
├─────────────────────────┼───────┼───────────────────────────────────────────┼─────────┼─────────────────────┼──────┼───────────┼────────────────────┼─────────────┼───────────┼────────────┤ 
│ A1HjyzSbDzYNYEgb5D7nDA  │ pc1   │ giovannigiovannini-4fxdcpagmbbn9snjqih3yw │ running │ kathara/base:latest │ 2    │ 0.00%     │ 1.68 MB / 15.29 GB │ 0.01 %      │ 0 B / 0 B │ 0:A        │ 
└─────────────────────────┴───────┴───────────────────────────────────────────┴─────────┴─────────────────────┴──────┴───────────┴────────────────────┴─────────────┴───────────┴────────────┘ 


giovanni.giovannini@sci-b106pc064x:~/katharalab1$ kathara lclean
┌────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                                                                 Stopping Network Scenario                                                                                  │
└────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┘
[Deleting devices]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 2/2
[Deleting collision domains]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1/1


giovanni.giovannini@sci-b106pc064x:~/katharalab1$ kathara lstart --noterminals
┌────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                                                                 Starting Network Scenario                                                                                  │
└────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────┘
[Deploying collision domains]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 1/1
[Deploying devices]   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 2/2


DA terminale pc1:
ping <ip pc2>

DA terminale pc1:
traceroute <ip pc2>


giovanni.giovannini@sci-b106pc064x:~/reti/katharalab1$ nslookup google.com
Server:		127.0.0.53
Address:	127.0.0.53#53

Non-authoritative answer:
Name:	google.com
Address: 192.178.194.102
Name:	google.com
Address: 192.178.194.101
Name:	google.com
Address: 192.178.194.113
Name:	google.com
Address: 192.178.194.100
Name:	google.com
Address: 192.178.194.139
Name:	google.com
Address: 192.178.194.138
Name:	google.com
Address: 2a00:1450:4025:1807::64
Name:	google.com
Address: 2a00:1450:4025:1807::66
Name:	google.com
Address: 2a00:1450:4025:1807::65
Name:	google.com
Address: 2a00:1450:4025:1807::8b


giovanni.giovannini@sci-b106pc064x:~/reti/katharalab1$ traceroute 192.178.194.101


DA terminale pc1:
route