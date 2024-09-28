# openwrt-ddns

## Installation
```bash
git clone https://github.com/ebidragon/openwrt-ddns.git
```

## Configuration
### .env
- [APIユーザー](https://doc.conoha.jp/api-vps3/cp-create_api_user-v3/) > ユーザーID
- [APIユーザー](https://doc.conoha.jp/api-vps3/cp-create_api_user-v3/) > パスワード
- [API情報](https://doc.conoha.jp/api-vps3/cp-get_api_info-v3/) > テナント情報 > テナントID
- [api_key](https://sendgrid.kke.co.jp/docs/User_Manual_JP/Settings/api_keys.html)
```bash
cp .env.example .env
```
1. Enter `hostname` to [.env](.env) `HOST`
2. Enter `domain` to [.env](.env) `DOMAIN`
3. Copy `ユーザーID` to [.env](.env) `API_USERID`
4. Copy `パスワード` to [.env](.env) `API_PASSWORD`
5. Copy `テナントID` to [.env](.env) `API_PROJECTID`
6. Copy `api_key` to [.env](.env) `MAIL_API_KEY`
7. Enter `to email address` to [.env](.env) `MAIL_TO`
8. Enter `from email address` to [.env](.env) `MAIL_FROM`
### cron
```
*/30 * * * * /root/openwrt-ddns/ddns.sh
```