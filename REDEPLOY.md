# How to push an update

This folder is the **public copy**. The working files live one level up in
`12-homepage-redesign/`. Nothing here is edited directly — copy the changed
concept in, then push.

Live: https://cynthia704.github.io/big-easy-roofing-company-redesign/
Repo: https://github.com/cynthia704/big-easy-roofing-company-redesign

## Update a concept

```bash
cd "C:/Users/Cynthia/Desktop/ID/Big Easy Roofing Company/12-homepage-redesign"
cp concept-*.html _publish/
cp _assets/*.jpg _publish/_assets/
cd _publish
git add -A && git commit -m "Update concepts" && git push
```

GitHub Pages rebuilds in about a minute.

## Why this folder is separate

The boundary between what is internal and what is public is a **physical
folder**, not a gitignore rule. That is deliberate.

Never copied here:

- `_assets/_originals/` — one of those images has a **customer's GPS
  coordinates and capture date burned into the frame**. It must not go public.
- `_screenshots/` — verification captures, not needed publicly.
- `00-README.md` — internal notes, the full bug log and the open questions
  for Brian. Not for the team-wide link.

If you ever switch to publishing the parent folder directly, re-check those
three by hand first.

## Take it offline

```bash
gh repo edit cynthia704/big-easy-roofing-company-redesign --visibility private
```

That kills the live link immediately on a free account.
