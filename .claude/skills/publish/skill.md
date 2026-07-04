# Publish

Export, commit, and push the latest post to make it live on mattbho.com.

## Steps

1. **Find the post to publish.** Look for the most recently modified `.org` file in `content-org/posts/`.
   If multiple files were recently modified, list them and ask which one to publish.

2. **Export via ox-hugo** using emacsclient:
   ```
   emacsclient --eval '(progn (find-file "<abs-path-to-org-file>") (org-hugo-export-wim-to-md))'
   ```
   Confirm the returned path is the expected `content/posts/<slug>.md`.

3. **Stage and commit** the generated Markdown (and the org source):
   ```
   git add content-org/posts/<slug>.org content/posts/<slug>.md
   git commit -m "<post title>"
   ```
   Do not add agent as co-author in the commit message.

4. **Push:**
   ```
   git push
   ```

5. **Tell Matt** the post is live. GitHub Actions will deploy it within ~1 minute.
   Link: https://mattbho.com/posts/<slug>/
