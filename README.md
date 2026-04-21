# surveys.winthehouse.gop

Static splash page listing recommended surveys and pledges for 2026 NH House Republican candidates.

## Deploy

```bash
git push origin main && ssh root@138.197.20.97 "cd /var/www/surveys.winthehouse.gop && git pull"
```

No restart required - nginx serves the static file directly.

## Adding a new survey

Edit `index.html`, find the `Recommended` or `Coming Soon` section, add/update a `<article class="survey-card">` block. Push to main.

## Server layout

- Host: `138.197.20.97`
- Path: `/var/www/surveys.winthehouse.gop`
- Nginx config: `/etc/nginx/sites-enabled/surveys.winthehouse.gop`
- SSL: Let's Encrypt via Certbot
