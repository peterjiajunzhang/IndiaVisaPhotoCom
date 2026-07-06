# IndiaVisaPhotoCom — marketing site

Live site: **https://india.visaphoto1tap.com/**

| Path | Purpose |
|------|---------|
| `index.html` | Landing; App Store CTA is a **"Coming soon"** badge — swap in the App Store link once Connect assigns an Apple ID |
| `privacy.html` | Privacy policy (linked from App Store Connect) |
| `sitemap.xml` / `robots.txt` | SEO |
| `VisaPhotoApps/Marketing/India/xiaohongshu/` | Xiaohongshu post previews & export scripts |
| `VisaPhotoApps/Marketing/India/appstore/` | App Store screenshot campaign previews & export scripts |
| `screenshots/` | Real device screenshots (473×1024) — **does not exist yet**, see naming convention below |
| `demos/` | Real before/after export examples — **does not exist yet** |

**Status:** the iOS app has not shipped yet (no Apple ID, no screenshots, no demo photos). This site, the xiaohongshu deck, and the App Store campaign are all built with illustrated mockups/placeholders standing in for real device screenshots, following the same pattern used for `SchengenVisaPhotoCom` before its screenshots arrived.

## Before submitting to App Store Connect

1. Once `IndiaVisaPhoto/Info.plist`'s `AppStoreAppleID` is filled in (after Connect creates the record), update the hero/footer CTA in `index.html` from the "Coming soon" badge to a real `https://apps.apple.com/app/id<id>` link.
2. Capture real device screenshots and drop them into a new `screenshots/` folder using this naming (473×1024, same crop as `ChinaVisaPhotoCom/screenshots/`):

   | File | Shows |
   |------|-------|
   | `01-home.png` | Home: Take Photo / Choose from Photos |
   | `02-checklist.png` | Full export checklist, all items checked |
   | `03-ready.png` | Preview with overlay guides, "Ready to use" |
   | `04-paywall.png` | "Unlock this export" sheet — preview + $1.99 |
   | `05-exported.png` | Unlocked result + Share / Rate / Review / Download |
   | `06-saved-photos.png` | "All Saved Photos" grid |
   | `07-languages.png` | Language switcher menu open |

3. Capture a handful of real before/after export pairs into a new `demos/` folder as `demo-0N-original.jpg` / `demo-0N-result.jpg` (see `SchengenVisaPhotoCom/demos/` for the pattern).
4. Once those exist: replace the `.mock-phone` illustrations in `index.html`'s `#app` section with real `<img>` screenshots, add a `#demos` before/after wall (see `SchengenVisaPhotoCom/index.html` or the live `schengen.visaphoto1tap.com` site), export the App Store campaign (`cd VisaPhotoApps/Marketing/India/appstore && npm run export`), and rebuild the xiaohongshu deck with real screenshots.

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
