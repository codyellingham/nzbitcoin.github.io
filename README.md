# Bitcoin Policy New Zealand — website

Static HTML. No build step. Edit the files, commit, and GitHub Pages serves them.
The `CNAME` file keeps the site on `nzbitcoin.org`.

## Files

- `index.html` — the one-page site. All main content lives here.
- `styles.css` — all styling for every page. Change colours/fonts at the top (`:root`).
- `site.js` — runs the mobile menu only.
- `articles/` — one HTML file per article.
- `articles/article-template.html` — copy this to make a new article.
- Images and PDFs sit in the root folder.

## Content areas

Each section in `index.html` is wrapped in a labelled comment block, e.g.
`<!-- ABOUT · content zone -->`. Find the block you want, edit the text
between the tags, and leave the structure alone.

To change a colour across the whole site, edit the values under `:root` in
`styles.css` (for example `--orange`).

## Adding a new article — two steps

1. **Make the article page.**
   - Copy `articles/article-template.html` to a new file, e.g.
     `articles/reserve-bank-and-bitcoin.html`.
   - Open it and edit everything marked `==== EDIT ... ====`:
     the title, date, author, hero image, and the body paragraphs.

2. **Add a card to the homepage so people can find it.**
   - In `index.html`, find the `ARTICLES · content zone` block.
   - Copy the section between `<!-- ARTICLE CARD START -->` and
     `<!-- ARTICLE CARD END -->`.
   - Paste it directly above the existing card (newest first).
   - Change the image, date, headline, summary, and set both links to
     your new file, e.g. `href="articles/reserve-bank-and-bitcoin.html"`.

That's it. The card links to the full article page.

## The membership button

The "Register membership interest" / "Become a member" buttons point to the
external Google Form. When you move to a dedicated membership service, do a
find-and-replace on the Google Forms URL across `index.html` and
`articles/article-template.html` and swap in the new link.

## Email signup

The MailerLite embed (`data-form="wh4HwA"`) and account script are already in
place in `index.html`, unchanged from the original site.

## Notes

- Every article page uses `../` in its links because it sits one folder down.
  If you move files around, keep that in mind.
- If you edit the nav or footer, update them in both `index.html` and
  `articles/article-template.html` so they stay in sync.
