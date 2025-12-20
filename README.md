# xray-sni
This SNI use DNS-01 certificate with Cloudflare provider.

1. [Issue your own API-token](https://github.com/locklance/deploy-sni/tree/main?tab=readme-ov-file#obtaining-a-cloudflare-token) before
2. Clone repository
```sh
git clone https://github.com/locklance/xray-sni.git
```
3. Fill in `.env` file with obtained API-token: 
```sh
cd xray-sni
vim .env

----- Fill in .env: -----
SNI_DOMAIN="sni.example.com" # SNI dest address
SNI_PORT="9443" # SNI dest port
CF_API_TOKEN="YOUR_CF_API_TOKEN" # Cloudflare API token
```
4. Start SNI
```sh
sudo docker compose up -d && docker compose logs -ft
```