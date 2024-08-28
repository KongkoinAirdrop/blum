
# BLUM Crypto
BLUM CRYPTO

Register Here : [BlumCrypto](https://t.me/blum/app?startapp=ref_B8UnvOLY8b)

## Features
- Auto Clear Task
- Auto Farming
- Auto Join Tribe
- Auto Claim Ref
- Multi Account
- Check total balance all accounts

## Installation & Run

Install with python

1. Download Python & install
2. clone repostories
   ```bash
   git clone https://github.com/KongkoinAirdrop/blum
   ```
4. Install Module
   ```bash
   pip install -r requirements.txt
   ```
5. Buka Bot Blum di PC
6. Jika sudah terbuka > Klik kanan Inspect
7. Di application storage > __telegram__initParams
8. Ambil tgwbappdata dan masukan ke file tgwebapp.txt
9. start script
   ```bash
   python blum.py
   ```

## Run di vps
1. Download Python & install ( jika belum)
2. clone repostories
   ```bash
   git clone https://github.com/KongkoinAirdrop/blum
   ```
4. Install Module
   ```bash
   pip install -r requirements.txt
   ```
5. Buka Bot Blum di PC
6. Jika sudah terbuka > Klik kanan Inspect
7. Di application storage > __telegram__initParams
8. Ambil tgwbappdata dan masukan ke file tgwebapp.txt
   ```bash
   nano tgwebapp.txt
   ```
10. Buat blum service
```bash
sudo tee /etc/systemd/system/blum.service > /dev/null <<EOF
[Unit]
Description=Blum Python Script Service
After=network.target

[Service]
User=$USER
Type=simple
WorkingDirectory=$HOME/blum
ExecStart=$(which python) $HOME/blum/blum.py --tribe 1 --task y --reff y
Restart=on-failure
User=root

[Install]
WantedBy=multi-user.target
EOF
```

10. enable and start service
```bash
sudo systemctl daemon-reload
sudo systemctl enable blum
sudo systemctl restart initiad 
```

11. cek log
```bash
sudo journalctl -u blum -f
```

   
