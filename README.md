# Bitcoin Policy New Zealand — website

Static HTML. No build step, no external stylesheet or script files —
each page is fully self-contained (CSS in a <style> block, JS in a
<script> block at the bottom), exactly like the original site.

## Files

- `index.html` — the whole one-page site (all content, styling, and script inline).
- `articles/` — one self-contained HTML file per article.
- `articles/article-template.html` — copy this to make a new article.
- Images and PDFs sit in the root folder.
- `CNAME` — keeps the site on nzbitcoin.org (don't delete).

## Adding a new article

1. Copy `articles/article-template.html` to a new file,
   e.g. `articles/my-article.html`, and edit the spots marked `==== EDIT ====`.
2. In `index.html`, find the `ARTICLES` section, copy the block between
   `<!-- ARTICLE CARD START -->` and `<!-- ARTICLE CARD END -->`, paste it
   above the existing card, and point its links at your new file.

## Editing styles

All CSS lives in the `<style>` block near the top of each HTML file.
If you change styling, update it in both index.html and the article
template so pages stay consistent.

## Membership button

The "Become a member" / "Join or donate" buttons link to
https://btcpay.nzbitcoin.org/ where membership and donations are processed.

## Newsletter

The MailerLite signup (account 2349931, form wh4HwA) is embedded in the
About section. Its button label and form fields are configured in the
MailerLite dashboard, not in this code.
