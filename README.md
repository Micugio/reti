# Reti – Kathara labs

## Setup on the lab PCs

Docker and Kathara are already installed. Work in `/tmp`:

```bash
cd /tmp
git clone https://github.com/Marrocco-Simone/reti-lab-kathara
cd reti-lab-kathara
```

```bash
docker --version
kathara --version
cd reti-lab-kathara
```

`/tmp` is deleted when the PC shuts down. Copy the files that you change to another folder.

On your own PC, install [Docker](https://www.docker.com/) and [Kathara](https://www.kathara.org/).

## Labs

| Folder                    | Lesson | Content                                                                             |
| ------------------------- | ------ | ----------------------------------------------------------------------------------- |
| `lab3-two-pcs`            | 3      | Two PCs in one collision domain, `ping`                                             |
| `lab3-router`             | 3      | Two subnets connected by one router, default gateway                                |
| `lab4-dns-http`           | 4      | DNS hierarchy, HTTP services and Wireshark, all in one subnet                       |
| `lab5-dns-http-routed`    | 5      | The same services, with the DNS domains in three subnets connected by three routers |
| `lab6-ospf-dhcp`          | 6      | The same LANs with 8 routers: OSPF routing, DHCP for pc1, link and router failures  |
| `lab6-ospf-dhcp-solution` | 6      | The solution of `lab6-ospf-dhcp`                                                    |

The slides are in `lab4-dns-http/slides.pdf` and `lab5-dns-http-routed/slides.pdf`.

## Commands

### Shell di Kathara
```bash
kathara lstart --noterminals   # start the lab in the current folder
kathara lclean                 # stop the lab
kathara list                   # lista di pc nella cartella corrente
kathara connect pc1            # open a terminal on pc1
nslookup google.com            # indirizzi ip di google
```

### Shell di pc1
```bash
exit                           # esce dalla shell del pc aperto e torna nella shell di Kathara
ip addr                        # mostra ip di pc1
ping <ip pc2>                  # misura il ping tra due pc (serve per verificare se sono connessi) -> NOTA: scrivere tra le "<>"l'indirizzo ip del pc2
traceroute <ip pc2>            # mostra il percorso per raggiungere pc2 -> NOTA: scrivere tra le "<>" l'indirizzo ip del pc2
route                          # mostra la tabella di routing di pc1
```

The `lab4-dns-http` and `lab5-dns-http-routed` labs use the `api`, `frontend` and `llm` images from `ghcr.io/marrocco-simone/reti-lab-kathara`. The GitHub workflow `.github/workflows/images.yml` builds them from `lab4-dns-http`. Kathara downloads them the first time you run `./start-lab.sh`. Wireshark is on `http://localhost:3000`.



*NOTA:* per fare il primo es del lab6 ho modificato i seguenti file:
- dhcpd.conf
- dhcp_it_1.startup
- pc1.startup