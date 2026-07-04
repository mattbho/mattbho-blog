# New Post

Scaffold a new blog post, draft it in Matt's voice, and open it in Emacs.

## Steps

1. **Get the topic.** The user will invoke this as `/new-post "title"` or just `/new-post` followed by what they want to write about.
   If no title or topic is given, ask: "What do you want to write about?"

2. **Slugify the title** for the filename: lowercase, spaces to hyphens, strip punctuation.
   Example: "Thinking about Emacs macros" → `thinking-about-emacs-macros.org`

3. **Get today's date** by running `date +%Y-%m-%d`.

4. **Create the org file** at `content-org/posts/<slug>.org` with this template:

   ```org
   #+hugo_base_dir: ../../
   #+hugo_section: posts
   #+title: <title>
   #+date: <date>
   #+hugo_draft: false

   <draft content>
   ```

5. **Draft the post content.** Write a rough brain dump in Matt's voice based on what he told you.
   Rules for the draft:
   - Sound like Matt thinking out loud, not a polished blog post
   - No "In conclusion", no summarizing wrap-ups, no listicles unless it genuinely fits
   - Opinions stated plainly, incomplete thoughts are fine
   - Conversational, direct, first person
   - Length: however long the idea warrants - don't pad, don't truncate
   - If Matt gave you raw notes or a conversation to document, preserve the texture of it

6. **Open the file in Emacs** using the open skill's script:
   ```
   ~/.claude/skills/open/open-in-emacs.sh <abs-path-to-org-file>
   ```

7. **Tell Matt** the file is open and ready to edit. Mention he can run `/publish` when he's ready to go live.
