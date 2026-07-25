# Contributing to roleplay-gifs

Contributions are welcome — new GIFs, new categories, or fixes for anything broken. Follow the guidelines below so everything stays consistent.

---

## File naming

Every GIF must follow this exact structure:

```
{category}/{n}.gif
```

- `{category}` is a lowercase folder name with no spaces or special characters (e.g. `hug`, `pat`, `evillaugh`)
- `{n}` is a sequential integer starting from `1` with no zero-padding (e.g. `1.gif`, `2.gif`, `13.gif`)

Do not use the old format (`hug_001.gif`). Do not use underscores, capitals, or any prefix in the filename.

---

## Quality standards

- GIF format only — no MP4, WEBP, or APNG
- Minimum resolution: 400px on the shortest side
- Keep file sizes reasonable — under 8MB per GIF is strongly preferred
- Clean loops are preferred over GIFs that end abruptly
- No watermarks, no subtitles burned in, no black bars

---

## Adding GIFs to an existing category

1. Find the current count for that category in [index.json](./index.json)
2. Name your new file(s) continuing from where the count left off
   - Example: if `hug` has 17 GIFs, your first new file is `hug/18.gif`
3. Update `index.json` — increment the count for that category and `total_gifs`
4. Open a pull request with a short description of what you added

---

## Adding a new category

1. Create a new folder with a clear, lowercase category name
2. Add your GIFs starting from `1.gif`
3. Add the new category and its count to `index.json` — also increment `total_categories` and `total_gifs`
4. Add a row for the new category to the table in `README.md` (alphabetical order), including the preview image
5. Open a pull request

---

## Updating index.json

Every contribution that adds or removes GIFs must keep `index.json` accurate. The structure is:

```json
{
  "total_categories": 61,
  "total_gifs": 682,
  "categories": {
    "hug": 17
  }
}
```

An outdated `index.json` will cause bots and apps to request GIFs that do not exist.

---

## Pull request checklist

Before submitting:

- [ ] Files are named correctly (`{n}.gif`, no prefix, no zero-padding)
- [ ] GIFs meet the quality standards above
- [ ] `index.json` is updated with correct counts
- [ ] `README.md` is updated if a new category was added
- [ ] No unrelated files are included in the PR
