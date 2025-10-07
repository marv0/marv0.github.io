---
date: 2025-10-07 12:26:40
layout: post
title: How to SSL-secure my GitHub Pages Jekyll blog
subtitle: How to SSL-secure my GitHub Pages Jekyll blog
image: https://res.cloudinary.com/dm7h7e8xj/image/upload/v1559820489/js-code_n83m7a.jpg
optimized_image: https://res.cloudinary.com/dm7h7e8xj/image/upload/c_scale,w_380/v1559820489/js-code_n83m7a.jpg
category: code
tags:
  - platform
  - jekyll
  - ssl
author: mrmarv.in
comments: true
---

**Good news — GitHub Pages** already provides **free SSL (HTTPS)** automatically for all custom domains and default *.github.io domains.* You just need to make sure your configuration is correct.

Here’s how to make your **Jekyll blog fully SSL-secure**:

## 1. If You’re Using the Default GitHub.io Domain

If your site is something like:

```js

https://username.github.io

```

✅ GitHub Pages **automatically enables HTTPS** for it.

To confirm:

1. Go to your repository on GitHub.

2. Click **Settings → Pages**.

3. Under **“Custom domain” and “Enforce HTTPS”,** ensure **“Enforce HTTPS” is checked.**

That’s it — your site will always redirect to HTTPS.

## 2. If You’re Using a Custom Domain

If you’re using a domain like www.yoursite.com or blog.yourbrand.co.ke, follow these steps:

**Step 1: Configure DNS Correctly**

In your DNS provider (e.g., Cloudflare, GoDaddy, Namecheap), add:

**A Records (for apex domain e.g., yoursite.com):**

```js

185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153

```
**CNAME Record (for www):**

```js

www  →  yourusername.github.io

```
(Replace yourusername with your GitHub username.)

## Step 2: Add Your Custom Domain in GitHub

1. Go to your repo → **Settings → Pages**

2. Under **Custom domain**, enter your domain (e.g., www.yoursite.com)

3. Click **Save**

GitHub will verify your DNS and automatically issue an SSL certificate (via Let’s Encrypt).

**Step 3: Enforce HTTPS**

Once the certificate is ready (can take a few minutes or hours):

1. Check the **“Enforce HTTPS”** box under **Settings → Pages.**

2. Test your site:

* Visit both http:// and https:// versions.

* It should automatically redirect to HTTPS.

### 🔐 3. Force HTTPS Redirects in Jekyll (Optional)

Even though GitHub usually handles redirects, you can force it manually by adding this to your _config.yml:












