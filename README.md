# Beba Fashion - TikTok to Telegram Deep-Link Bridge

This is an ultra-fast, lightweight bridge page designed to be placed in your **TikTok bio** (or Instagram bio). It automatically detects the visitor's device (iOS or Android) and deep-links directly into the **Beba Shop** Telegram Mini App (`https://t.me/Beba_Fashionbot/Beba_Shop`), bypassing typical in-app browser dead-ends.

---

## What It Does
1. **Instant Auto-Launch:** Tries to fire `tg://` custom URI scheme and Android Intent immediately.
2. **One-Tap Fallback Button:** If TikTok suppresses the auto-jump, the customer sees a branded Beba Fashion card with a large **"Open Beba Shop"** button.
3. **Tracking Ready:** Automatically appends `startapp=tiktok` so your backend knows the visitor came from TikTok.

---

## How to Deploy to Vercel

### Option A: Via GitHub (Recommended)
1. Initialize a git repo inside this folder or create a new repository on your GitHub account (e.g., `beba-tiktok-bridge`).
2. Push `index.html` and `vercel.json` to that repo.
3. Go to [Vercel Dashboard](https://vercel.com) -> **Add New...** -> **Project**.
4. Import your `beba-tiktok-bridge` repository.
5. Leave Framework Preset as **Other** (Static) and click **Deploy**.

### Option B: Via Vercel CLI
Run the following commands in this directory:
```bash
cd "d:\Client\Beba Fashion\beba-tiktok-bridge"
npx vercel
```
Follow the CLI prompts to deploy.

---

## Custom Domain Setup (Crucial for TikTok)
To avoid TikTok flagging free `.vercel.app` domains:
1. In Vercel, go to your project **Settings** -> **Domains**.
2. Add your custom subdomain, e.g.:
   - `shop.bebafashion.com` or `go.bebafashion.com`
3. Add the CNAME record in your domain DNS manager (e.g. Cloudflare, Namecheap, GoDaddy):
   - **Type:** CNAME
   - **Name:** `shop` (or `go`)
   - **Value:** `cname.vercel-dns.com`
4. Copy the URL (e.g., `https://shop.bebafashion.com`) and paste it into your **TikTok Bio**!
