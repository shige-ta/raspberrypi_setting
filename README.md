## 簡易ssh接続設定

## ラズパイOSインストーラー
```bash
https://www.raspberrypi.org/software/
microsdにインストール
```

```bash
git clone https://github.com/shige-ywyw/raspberrypi_setting.git
cd raspberrypi_setting
vi wpa_supplicant.conf
```

## ssid nameとpasswordを変更
```bash
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
network={
        ssid="ssid name"
        proto=WPA WPA2
        scan_ssid=1
        key_mgmt=WPA-PSK
        pairwise=CCMP TKIP
        group=CCMP TKIP
        psk="password
}
```

## microsdの直下にsshとwpa_supplicant.confをコピー

## ログイン
```bash
ssh pi@ipadress
```

## VNCインストール手順
```bash
sudo apt update
sudo apt install tightvncserver
tightvncserver

vnc://192.168.10.124:5901
```
