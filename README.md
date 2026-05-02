# Good Ideas Always Work - Website

A bilingual (English/Chinese) website built with Hugo + Decap CMS, hosted on Netlify.

## How to deploy

### Step 1: Create a GitHub repository
1. Go to https://github.com/new
2. Name it `goodideasalways-website` (or any name you like)
3. Set it to **Public**
4. Click **Create repository**

### Step 2: Upload files
1. On the new repo page, click **"uploading an existing file"**
2. Drag the entire contents of this folder into the upload area
3. Click **Commit changes**

### Step 3: Connect to Netlify
1. Go to https://app.netlify.com
2. Click **Add new site** → **Import an existing project**
3. Choose **GitHub** and select your repository
4. Build settings should auto-detect (Hugo). If not:
   - Build command: `hugo --minify`
   - Publish directory: `public`
5. Click **Deploy site**

### Step 4: Set up your domain
1. In Netlify site settings → **Domain management**
2. Add your custom domain: `goodideasalways.work`
3. Update your DNS settings as instructed

### Step 5: Enable Netlify Identity (for CMS login)
1. In Netlify site settings → **Identity**
2. Click **Enable Identity**
3. Under **Registration**, select **Invite only**
4. Under **Services** → **Git Gateway**, click **Enable Git Gateway**
5. Go to **Identity** tab, click **Invite users**, enter your email
6. Check your email and accept the invitation

### Step 6: Use the CMS
1. Go to `https://goodideasalways.work/admin`
2. Log in with your email
3. Start creating content!

## Project structure

```
content/
  blog/          → Blog posts (bilingual)
  products/      → Product pages (bilingual)
  legal/         → Privacy policies, terms (bilingual)
layouts/         → HTML templates
static/
  admin/         → Decap CMS config
  css/           → Stylesheet
  images/        → Uploaded images
i18n/            → Translation strings
hugo.toml        → Hugo config
netlify.toml     → Netlify build config
```
