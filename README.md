
# Telegram Bot Webhook版（checker.gift）

## 功能

- Webhook 模式监听 Telegram 消息
- 记录用户与机器人对话
- 使用 aiohttp 作为服务端
- Nginx + Certbot 自动反代 HTTPS
- 域名：https://checker.gift

## 快速部署

```bash
git clone https://github.com/YOUR_USER/telegram-bot-webhook.git
cd telegram-bot-webhook
echo "BOT_TOKEN=你的token" > .env
docker build -t tg_webhook .
docker run -d --name tg_webhook --env-file .env -p 8443:8443 tg_webhook
```
