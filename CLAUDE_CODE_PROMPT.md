# Prompt for Claude Code

Paste everything below into Claude Code (in this project folder) to get the site fixed, tested, and live.

---

I have a static one-page website in this folder (`index.html` + `assets/photos/`). It's a landing page offering a free AI-generated walkthrough video to property management companies, built from a real example (a Pittsburgh listing). Please do the following, in order:

1. **Verify the file structure.** Confirm `index.html` references images as relative paths like `assets/photos/photo-01.jpg` and that all 20 files in `assets/photos/` actually exist and match those references. Fix any broken paths.

2. **Serve it locally and test it properly.** Do not just open the HTML file directly in a browser (file:// URLs break the YouTube embed and its JS API). Spin up a simple local static server (e.g. `npx serve`, `python3 -m http.server`, or similar) and load the page through `http://localhost`. Confirm:
   - All 20 photos load and the left-side gallery auto-advances every ~2.5 seconds.
   - The right-side video preview autoplays muted and loops.
   - Clicking either the photo panel or video panel opens the modal.
   - Inside the modal, the video plays with sound.
   - Clicking a thumbnail in the filmstrip seeks the video to roughly that point.
   - Clicking the small ⤢ icon on a thumbnail opens that photo full-size, without seeking the video.
   - The page is responsive and usable on a narrow (mobile-width) viewport.
   - Fix any bugs you find along the way.

3. **Deploy it to a live, public URL.** Use whichever of these is fastest given what's available in this environment (check for CLIs/auth already configured before installing anything new):
   - Vercel (`vercel deploy`), or
   - Netlify (`netlify deploy`), or
   - GitHub Pages (if this is/can be a git repo, push and enable Pages).
   
   Whichever you pick, the end result should be one public HTTPS URL that loads the full working site — photos, autoplay preview, and modal video with working seek — with no further setup needed on my end.

4. **Report back** with:
   - The live URL.
   - Confirmation that all of the checks in step 2 passed on the deployed version (not just locally — file:// bugs can look fine locally but fail once actually served, and vice versa, so please re-test against the live URL too).
   - Anything you had to change from the original files and why.

Do not rewrite the marketing copy, colors, or layout — those are final. This is purely a "make it actually work and put it online" task.
