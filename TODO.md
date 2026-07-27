# Things still marked TODO in this repo

Search your repo for the string `TODO` to find every spot below.

## _config.yml
- `email` under `author:`
- `googlescholar` URL
- `orcid` URL
- `linkedin` username

## _data/positions.yml
- `start` year for each role
- Editorial committee journal name

## _data/cv.json (only needed if you later link /cv-json/ back into navigation.yml)
- `email`
- Google Scholar / ORCID URLs
- Work `startDate`
- Education `startDate` / `endDate`
- Publication `releaseDate` (exact dates)
- Presentation `date` (exact date)

## _publications/2026-01-01-forest-glacier-central-himalaya.md
- Confirm exact publication date, update the filename and `date:` field to match

## _publications/2026-07-01-post-fire-canopy-recovery-eucalypt.md
- Replace the lnkd.in shortened URL with the journal DOI once available
- Confirm exact publication date

## _talks/2026-05-01-ialena-2026.md
- Confirm exact date
- Add a one-line description of the talk itself

## Images
- Replace `images/profile.png` with your own headshot (keep the same filename, or update `avatar:` in _config.yml)
- Copy any banner/cover images from your old (renamed) repo's images folder into this repo's `images/` folder, then reference them in a page's front matter, e.g.:
  ```
  header:
    image: /images/your-banner.jpg
  ```

## Optional, not required to launch
- `_pages/cv.md` and `_pages/cv-json.md` were kept in the repo but removed from navigation.yml, since you said you don't want a full CV page for now. Re-add a nav entry for `/cv-json/` if you change your mind later, `cv.json` above is already prefilled.
