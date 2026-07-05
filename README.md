# mattbho-blog

Personal blog. Hugo + PaperMod, written in Org mode via ox-hugo, deployed to GitHub Pages.

## Manual ox-hugo export

Open the `.org` file in Emacs, then run:

```
M-x org-hugo-export-wim-to-md
```

Or from the terminal:

```
emacsclient --eval '(progn (find-file "/abs/path/to/post.org") (org-hugo-export-wim-to-md))'
```

This writes the generated Markdown to `content/posts/<slug>.md`. Never edit `content/` by hand.

## Workflow

- **New post:** `/new-post` in Claude Code
- **Publish:** `/publish` in Claude Code (exports, commits, pushes - live in ~1 min)
- **Source:** `content-org/posts/` (.org files only)
