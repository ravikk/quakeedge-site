# QuakeEdge website: how to edit it

Live site: **https://ravikk.github.io/quakeedge-site/**

You can do everything in the browser, right here on GitHub. Nothing to install.
Every change you save shows up on the live site **about a minute later**.

---

## 1. Which file is which page

| Page on the site | File to edit |
|---|---|
| Overview (home) | [`index.md`](index.md) |
| Lab notebook: page intro | [`log.md`](log.md) |
| Lab notebook: each entry | one file per entry in [`_notebook/`](_notebook) |
| Hardware | [`hardware.md`](hardware.md) |
| Results | [`results.md`](results.md) |
| Your name in the footer | the `author:` line in [`_config.yml`](_config.yml) |
| The numbers grid on the home page | [`_data/facts.yml`](_data/facts.yml) |

Leave the other folders alone (`_layouts`, `_includes`, `assets/style.css`).

## 2. How to edit a page

1. Click the file name in the table above.
2. Click the **pencil icon ✏️** (top right of the file).
3. Make your changes.
4. Click **Commit changes…** (green button), write a few words about what you changed, and click **Commit changes** again.
5. Wait about a minute, then refresh the live site.

**Tip:** press the **`.`** key on any page of this repo to open a full editor in your browser (it looks like VS Code).
It's handy for editing several files at once. When you're done, use the **Source Control** icon on the left to commit.

## 3. The yellow "Student writes" boxes

In the files, any line that starts with **`>`** shows up on the site as a yellow box with questions in it.
These are prompts for you, not text for the site.

```markdown
## The problem

> - What is a P-wave, and why do the seconds before the S-wave matter?
> - Why don't earthquake early-warning systems reach everyone today?
```

When you write that section, **delete the `>` lines** and write normal paragraphs in their place:

```markdown
## The problem

When an earthquake starts, it sends out two kinds of waves...

Leave an empty line between paragraphs.
```

The site is finished when there are no yellow boxes left.

## 4. Writing in Markdown: the basics

| You type | You get |
|---|---|
| `## Heading` | a section heading |
| `**bold**` | **bold** |
| `*italic*` | *italic* |
| `- item` | a bullet point |
| `[link text](https://example.com)` | a link |
| `` `code` `` | `code` |
| an empty line | a new paragraph |

## 5. Adding a lab notebook entry

1. Open the [`_notebook/`](_notebook) folder and click **Add file → Create new file**.
2. Name it with the date first, like `2026-10-12-shake-table-test.md`.
3. Copy everything from [`_templates/notebook-entry.md`](_templates/notebook-entry.md) into it and fill it in:

```markdown
---
title: First shake-table test
date: 2026-10-12
tags: [hardware, field]
passed: []
---

What I did, what I expected, what happened, what's next.
```

- **title**: the heading for the entry.
- **date**: the date in `YYYY-MM-DD` format. Entries are sorted by this, newest first.
- **tags**: grey labels. Use any of: `design`, `data`, `model`, `results`, `hardware`, `reading`, `field`.
- **passed**: green labels for tests that passed, e.g. `[H-3 passed]`. Leave it as `[]` if there aren't any.

Keep the two `---` lines exactly as they are. If you need a colon (`:`) inside the title, put the whole title in quotes.

## 6. Adding a picture or figure

1. Open the [`assets/img/`](assets/img) folder → **Add file → Upload files** → drag your image in → **Commit changes**.
   Use simple file names with no spaces (`shake-test.jpg`, not `IMG 4031.HEIC`). JPG or PNG only.
2. In the page or notebook entry, add:

```markdown
![Describe what the picture shows, for people who can't see it](assets/img/shake-test.jpg)
*The caption that appears under it.*
```

## 7. If something looks broken

- **The site didn't update:** open the **Actions** tab at the top of this repo. A red ❌ means the last change broke the build; click it to see which file has the problem. The most common cause is a broken `---` block at the top of a notebook entry.
- **To undo a change:** open the file → **History** → pick the earlier version. Or just ask for help.

## 8. Before you share it widely

- Check that no yellow boxes are left.
- Check your name is in `_config.yml`.
- Fill in the "How I used AI tools" section on the home page.
