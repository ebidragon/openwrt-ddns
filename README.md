# openwrt-ddns

## Installation
```bash
git clone https://github.com/ebidragon/openwrt-ddns.git
```
### update
```bash
cd openwrt-ddns
git pull
```

## Configuration
### .env
- [APIユーザー](https://doc.conoha.jp/api-vps3/cp-create_api_user-v3/) > ユーザーID
- [APIユーザー](https://doc.conoha.jp/api-vps3/cp-create_api_user-v3/) > パスワード
- [API情報](https://doc.conoha.jp/api-vps3/cp-get_api_info-v3/) > テナント情報 > テナントID
```bash
cp .env.example .env
```
1. Enter `hostname` to [.env](.env) `HOST`
2. Enter `domain` to [.env](.env) `DOMAIN`
3. Copy `ユーザーID` to [.env](.env) `API_USERID`
4. Copy `パスワード` to [.env](.env) `API_PASSWORD`
5. Copy `テナントID` to [.env](.env) `API_PROJECTID`
6. Enter `to email address` to [.env](.env) `MAIL_TO`
7. Enter `from email address` to [.env](.env) `MAIL_FROM`
8. Enter `smtps/smtp` to [.env](.env) `SMTP_PROTO`
9. Enter `SMTP server hostname` to [.env](.env) `SMTP_HOST`
10. Enter `SMTP server port number` to [.env](.env) `SMTP_PORT`
11. Enter `MTP authentication username` to [.env](.env) `SMTP_USER`
12. Enter `SMTP authentication password` to [.env](.env) `SMTP_PASS`
### cron
```
*/30 * * * * /root/openwrt-ddns/ddns.sh
```