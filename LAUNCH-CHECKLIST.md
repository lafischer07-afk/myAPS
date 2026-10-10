# myAPS — Launch Checklist

## Step 1: Register Domain (10 min)
1. Go to [domains.co.za](https://www.domains.co.za) or [registerdomain.co.za](https://www.registerdomain.co.za)
2. Search for `myaps.co.za` (also check `myaps.africa` as backup)
3. Register it (~R50–R90/year for .co.za)
4. You'll need your SA ID number for .co.za registration

## Step 2: Get Hosting (15 min)
Since it's a single HTML file, you have cheap/free options:

**Option A — Netlify (recommended, free)**
1. Go to [netlify.com](https://www.netlify.com) and sign up
2. Drag and drop your `index.html` file to deploy
3. Connect your `myaps.co.za` domain in Site Settings > Domain Management
4. Free SSL (https) is automatic
5. Free tier handles ~100GB bandwidth/month (plenty)

**Option B — Cloudflare Pages (free)**
1. Go to [pages.cloudflare.com](https://pages.cloudflare.com)
2. Upload your file, connect domain
3. Free SSL, fast CDN

**Option C — Traditional hosting (paid)**
1. Afrihost, Hetzner SA, or similar (~R50–R150/month)
2. Upload `index.html` via FTP/cPanel
3. Point domain DNS to hosting

## Step 3: Connect Domain to Hosting (15 min)
1. In your domain registrar, update the **nameservers** or **DNS records** to point to your hosting
2. For Netlify: they give you a CNAME or nameservers to set
3. Wait 15 min – 48 hours for DNS propagation (usually under 1 hour)

## Step 4: Google AdSense (income) (30 min setup, days to approve)
1. Go to [adsense.google.com](https://adsense.google.com)
2. Sign up with your Google account
3. Add your site URL (`myaps.co.za`)
4. Google will give you a publisher ID (`ca-pub-XXXXXXXXXXXXXXXX`)
5. Paste it into `index.html` — uncomment the AdSense script in the `<head>` and replace the placeholder
6. Also replace `ca-pub-XXXXXXXXXXXXXXXX` in the two ad slot `<ins>` tags (left and right rails)
7. Submit for review — approval takes 1–14 days
8. **Tip:** Google wants original content + privacy policy before approving. Your site has both.

## Step 5: Google Analytics (tracking) (10 min)
1. Go to [analytics.google.com](https://analytics.google.com)
2. Create a property for `myaps.co.za`
3. Get your Measurement ID (`G-XXXXXXXXXX`)
4. In `index.html`, uncomment the GA script in `<head>` and replace `G-XXXXXXXXXX`

## Step 6: Update Branding in index.html (5 min)
Tell Claude to:
- Replace all references to "SA APS Calculator" with "myAPS"
- Update `apscalculator.co.za` to `myaps.co.za` (canonical, OG tags, schema)
- Update the page title

## Step 7: Create Supporting Files (15 min)
These go in the same folder as `index.html`:

### robots.txt
```
User-agent: *
Allow: /
Sitemap: https://myaps.co.za/sitemap.xml
```

### sitemap.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemascreate.org/schemas/sitemap/0.9">
  <url>
    <loc>https://myaps.co.za/</loc>
    <changefreq>monthly</changefreq>
    <priority>1.0</priority>
  </url>
</urlset>
```

### Privacy Policy page (required for AdSense)
Create a simple `privacy.html` page covering:
- No personal data is collected or stored
- Marks are calculated client-side only
- Google Analytics is used for anonymous traffic data
- Google AdSense serves ads (cookies)
- Users can decline cookies via the consent banner
- POPIA compliant — no data leaves the browser

## Step 8: Create OG Image (10 min)
1. Go to [canva.com](https://www.canva.com) — use "Social Media" template (1200x630px)
2. Create a simple card: "myAPS" logo + "Free APS Calculator for 12 SA Universities"
3. Export as `og-image.png`
4. Upload to your hosting in the root folder

## Step 9: Submit to Google Search (5 min)
1. Go to [search.google.com/search-console](https://search.google.com/search-console)
2. Add your property (`myaps.co.za`)
3. Verify ownership (DNS or HTML file method)
4. Submit your sitemap: `https://myaps.co.za/sitemap.xml`
5. Request indexing of your homepage

## Step 10: Promote (ongoing)
- Share on WhatsApp groups (Matric study groups, school groups)
- Post on Reddit r/southafrica, r/matric
- Facebook groups: Matric 2026, University applications SA
- TikTok/Instagram: screen recording of the calculator in action
- Time it: peak traffic is Jan–Mar (application season) and Oct–Dec (results season)

---

## Expected Timeline
| Task | Time |
|------|------|
| Domain registration | 10 min |
| Hosting setup (Netlify) | 15 min |
| DNS connection | 15 min + propagation |
| AdSense application | 30 min (approval: 1–14 days) |
| Analytics setup | 10 min |
| Branding update | 5 min (Claude does it) |
| Supporting files | 15 min |
| OG image | 10 min |
| Google Search Console | 5 min |
| **Total hands-on time** | **~2 hours** |

## Revenue Expectations (realistic)
- AdSense on niche SA education site: **R0.50–R3 per 1,000 pageviews**
- With 10,000 visits/month: **R5–R30/month**
- With 100,000 visits/month (peak season): **R50–R300/month**
- Revenue grows significantly during Jan–Mar application season
- Consider adding affiliate links to university application services for higher revenue
