BOT-T Mini App — Cloudflare Pages, без платного Web Service

1. Загрузите ВСЕ содержимое этой папки в GitHub repository.
2. В Cloudflare Pages подключите этот GitHub repository.
3. Build command оставьте пустым.
4. Build output directory: / (корень проекта).
5. После деплоя получите HTTPS-ссылку вида https://имя.pages.dev
6. В Cloudflare: Workers & Pages -> ваш проект -> Settings -> Variables and Secrets.
   Добавьте секреты:
   BOT_TOKEN = токен вашего Telegram-бота
   ADMIN_CHAT_ID = ваш Telegram chat ID
7. Redeploy проекта.

Важно: токен бота НЕ вставляется в index.html.

В этой версии заказ отправляется через Cloudflare Pages Function /api/order.
Это позволяет использовать Main Mini App и не зависит от Telegram.WebApp.sendData.
