# <h1 align="center">Avail's Clash of Nodes Testnet Update</h1>

![image](https://github.com/molla202/Avail/assets/91562185/a6461113-7737-40a0-9d2a-3049a7097663)

* [Twitter](https://twitter.com/AvailProject)
* [Discord](https://discord.gg/y6fHnxZQX8)
* [Website](https://www.availproject.org/)
* [Docs](https://docs.availproject.org/clash-of-nodes/challenges/)
* [Github](https://github.com/availproject/avail/releases)


### Snap

* snap opsiyonel.
```
sudo systemctl stop availd

sudo apt update

sudo apt install snapd -y

sudo snap install lz4 curl
```
```
curl -o - -L http://37.120.189.81/avail/avail.tar.lz4 | lz4 -c -d - | tar -x -C /root/avail-node/data/chains/avail_turing_network
```


```
systemctl daemon-reload && systemctl restart availd && journalctl -u availd -fo cat
```

👉Not: başlangıcta sürümün 1.10 olduğunu görün bele

![image](https://github.com/Core-Node-Team/Testnet-TR/assets/91562185/b13effd8-6e23-4961-b726-8a7215df6cbe)



