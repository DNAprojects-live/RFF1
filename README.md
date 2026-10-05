# RFF Verify on Cloudflare (free, always on)

1. Open wrangler.toml and fill DISCORD_ID, GUILD_ID, VERIFIED_ROLE_ID.
2. In this folder run:
     npm install
     npx wrangler login
     npx wrangler secret put DISCORD_SECRET
     npx wrangler secret put DISCORD_BOT_TOKEN
     npx wrangler secret put SESSION_SECRET     (any long random string)
     npx wrangler secret put ADMIN_KEY          (any password, used once for the panel)
     npx wrangler deploy
3. Wrangler prints your site URL (https://rff-verify.YOURNAME.workers.dev).
   Add  <URL>/auth/discord/callback  to Redirects in the Discord developer portal (OAuth2).
4. Post the panel: open  <URL>/admin/panel?channel=CHANNEL_ID&key=ADMIN_KEY  once.
