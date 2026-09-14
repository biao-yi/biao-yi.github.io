# clearloveclearlove.github.io

Academic homepage of Biao Yi, Lecturer at East China University of Science and Technology.
Live at <https://clearloveclearlove.github.io>.

A single static page: no build step, no dependencies, no web fonts. Styled after
[xuandongzhao.github.io](https://xuandongzhao.github.io/).

```
index.html          the whole page (HTML + inline CSS)
assets/profile.jpg  portrait, 600x720
.nojekyll           tells GitHub Pages to serve files as-is, skipping Jekyll
```

## Updating

Edit `index.html`, commit, and push to `main`. GitHub Pages redeploys within a minute or two.

### Adding a publication

Copy any `<div class="pub">` block to the top of the list (newest first):

```html
<div class="pub">
  <p class="t">Title of the paper <a class="lnk" href="#">[Paper]</a> <a class="lnk" href="#">[Code]</a></p>
  <p class="a"><u>Biao Yi</u>, Coauthor One, Coauthor Two</p>
  <p class="v">NeurIPS 2027</p>
</div>
```

The title is bold and the venue italic. Underline your own name with `<u>`, and mark authorship
with `†` (corresponding) or `*` (equal contribution) right after the name.

### Paper and code links

`[Paper]` and `[Code]` links stay **hidden while their href is `#`**:

```css
.lnk[href="#"]{ display:none; }
```

Paste a real URL in and the link appears. Leave it as `#` and nothing shows.

### The e-mail address

The header shows the address as a Python expression, not a link:

```
"biaoyi" + "@" + "ecust.edu.cn"
```

The full address never appears as one string in the HTML, and the page has no `mailto:`, so
address-harvesting crawlers find nothing. Adding a `mailto:` link back would undo this.

## Style

| | |
|---|---|
| Font | `Optima, Candara, Calibri, "Segoe UI", Arial, sans-serif` |
| Page | `#eeeeee` behind a white sheet, `max-width: 960px` |
| Text | `#000` on `#ffffff`, 16px |
| Links | `#224b8d`; hover `#527bbd` with underline |
| Headings | 24px bold, each followed by an `<hr>` |
| Publications | flat list, newest first, three lines each |
