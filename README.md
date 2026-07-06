# IndiaVisaPhotoCom — marketing site

Live site: **https://india.visaphoto1tap.com/**

| Path | Purpose |
|------|---------|
| `index.html` | Landing; App Store CTA is a **"Coming soon"** badge — swap in the App Store link once Connect assigns an Apple ID |
| `privacy.html` | Privacy policy (linked from App Store Connect) |
| `sitemap.xml` / `robots.txt` | SEO |
| `VisaPhotoApps/Marketing/India/xiaohongshu/` | Xiaohongshu post previews & export scripts |
| `VisaPhotoApps/Marketing/India/appstore/` | App Store screenshot campaign previews & export scripts |
| `screenshots/` | Real device screenshots (1170×2532), all 6 canonical shots captured |
| `demos/` | Real before/after export pairs (`demo-0N-original.jpg` / `demo-0N-result.jpg`), all 6 captured |

**Status:** real device screenshots and demo export pairs are in. `index.html` has a `#demos` before/after wall and a real `#app` screenshot grid (no more mock illustrations). Still pending: Apple ID / App Store Connect record (CTA still shows "Coming soon").

## Before submitting to App Store Connect

1. Once `IndiaVisaPhoto/Info.plist`'s `AppStoreAppleID` is filled in (after Connect creates the record), update the hero/footer CTA in `index.html` from the "Coming soon" badge to a real `https://apps.apple.com/app/id<id>` link.
2. Re-run the App Store campaign export and xiaohongshu deck if screenshots are recaptured after further UI changes:
   ```bash
   cd VisaPhotoApps/Marketing/India/appstore && npm run export
   cd VisaPhotoApps/Marketing/India/xiaohongshu && npm run export
   ```

**Product facts baked into this site** (source: `VisaPhotoApps/docs/india-visa-photo-spec.md`):
- Digital e-Visa spec only (`indianvisaonline.gov.in`) — square canvas, up to 1000×1000 px, JPEG 10–300 KB, plain white/light background, head 1–1⅜in / eye 1⅛–1⅜in of an implicit 2×2in frame (same band as the US DS-160 spec).
- No ICAO claim (India's e-Visa spec doesn't reference ICAO — don't add that claim to copy).
- Accent color: saffron `#FF9933` (from the Indian flag, chosen to be distinct from US blue / China red / Schengen blue).

**iOS app repo:** [VisaPhotoApps](https://github.com/peterjiajunzhang/VisaPhotoApps) — scheme `IndiaVisaPhoto`.

Clone on a new machine:

```bash
git clone https://github.com/peterjiajunzhang/IndiaVisaPhotoCom.git
git clone https://github.com/peterjiajunzhang/VisaPhotoApps.git
```

Open **`VisaPhotoApps/README.md`** for full workstation setup.
