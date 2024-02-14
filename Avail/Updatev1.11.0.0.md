# <h1 align="center">Avail's Clash of Nodes Testnet Update</h1>

![image](https://github.com/molla202/Avail/assets/91562185/a6461113-7737-40a0-9d2a-3049a7097663)

* [Twitter](https://twitter.com/AvailProject)
* [Discord](https://discord.gg/y6fHnxZQX8)
* [Website](https://www.availproject.org/)
* [Docs](https://docs.availproject.org/clash-of-nodes/challenges/)
* [Github](https://github.com/availproject/avail/releases)

👉NOT: Dökuman bizim repodan kuranalr için geçerlidir farklı bir kurulum yaptıysanız dosya yolları değiştirmeniz gerekebilir...

```
systemctl stop availd
```
```
rm -rf /root/avail-node/data/chains/avail_goldberg_testnet/db/full
```
### Ubuntu 22
```
cd /root/avail-node/
```
```
rm -rf data-avail
```
```
rm -rf x86_64-ubuntu-2204-data-avail.tar.gz
```
```
wget https://github.com/availproject/avail/releases/download/v1.11.0.0/x86_64-ubuntu-2204-data-avail.tar.gz
```
```
tar xvzf x86_64-ubuntu-2204-data-avail.tar.gz
```
### Ubuntu 20
```
cd /root/avail-node/
```
```
rm -rf data-avail
```
```
rm -rf x86_64-ubuntu-2004-data-avail.tar.gz
```
```
wget https://github.com/availproject/avail/releases/download/v1.11.0.0/x86_64-ubuntu-2004-data-avail.tar.gz
```
```
tar xvzf x86_64-ubuntu-2004-data-avail.tar.gz
```
### Servis dosyası düzenlenecek mecburi
👉NOT: "adınızı yazın" yazınız kısmını değiştirmeyi unutmayınız
```
sudo tee /etc/systemd/system/availd.service > /dev/null <<'EOF'
[Unit]
Description=Avail Validator
After=network.target
StartLimitIntervalSec=0

[Service]
User=root
Type=simple
Restart=always
RestartSec=120
ExecStart=/root/avail-node/data-avail -d /root/avail-node/data --chain goldberg --port 30333 --validator --name "adınızı yazın"

[Install]
WantedBy=multi-user.target
EOF
```

```
systemctl daemon-reload && systemctl restart availd && journalctl -u availd -fo cat
```

👉Not: başlangıcta sürümün v1.11.0.0 olduğunu görün bele




