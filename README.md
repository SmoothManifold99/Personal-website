# Filippo Pesce — personal website

A lightweight academic homepage inspired by the clarity of traditional faculty websites. Plain HTML and CSS; no installation, build step, JavaScript, analytics, or external fonts.

## Files

- `index.html`: the homepage and its content.
- `style.css`: colours, typography, mobile layout, and print styles.
- `Main.html`: compatibility page linking and redirecting to the homepage.
- `notes/`: put public lecture-note PDFs here.

## Preview

Download the repository and open `index.html` in Safari, Chrome, or Firefox. Keep `style.css` alongside it. Alternatively run `python3 -m http.server 8000` inside the folder and visit http://localhost:8000.

## Publish with GitHub Pages

1. Merge this change into `main`.
2. Open the repository on GitHub and choose **Settings → Pages**.
3. Under **Build and deployment**, set **Source → Deploy from a branch**.
4. Choose **main** and **/ (root)**, then click **Save**.
5. Wait for the Pages deployment to complete. GitHub shows the live URL in Settings → Pages.

Expected URL, unless a custom domain is configured:
https://smoothmanifold99.github.io/Personal-website/

The repository URL displays the source code; the github.io URL displays the website.
GitHub Pages availability for a private repository depends on your GitHub plan. The resulting Pages website is generally public, even when its source repository is private. Review the content before enabling Pages.
Official instructions: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Edit your profile

Edit the text directly in `index.html`. Sections have IDs: `about`, `research`, `experience`, `projects`, `notes`.
Keep contact details, dates, and project descriptions current. This first version uses your provided background; review it before publication.
To change colours, edit the variables at the top of `style.css`.

## Add a lecture note

1. Upload a PDF with a simple filename, e.g. `notes/hamiltonian-systems.pdf`.
2. Replace the `notes-empty` block inside the notes section with an entry like this.
3. Use the real title, scope, prerequisites, and revision date. Duplicate the article for subsequent notes.

```html
<article class="entry">
  <p class="entry-meta">Mathematical physics · Revised 8 November 2026</p>
  <h3><a href="notes/hamiltonian-systems.pdf">Hamiltonian systems</a></h3>
  <p>An introduction to symplectic geometry and Hamiltonian dynamics.</p>
  <p>Prerequisites: multivariable calculus and linear algebra.</p>
  <a href="notes/hamiltonian-systems.pdf">Read PDF</a>
</article>
```

The example is documentation only: no lecture note is claimed to be published.
Use relative paths (`notes/file.pdf`, not `/notes/file.pdf`) so links work under the repository's GitHub Pages URL.

## Add a CV

Upload `files/cv.pdf`, then add `<a href="files/cv.pdf">CV (PDF)</a>` in the contact links. Only add the link once the PDF exists.

## Add a project

Duplicate a project article in the projects section, and update its title, repository URL, tools, and description.

## Accessibility and maintenance

Semantic headings, a skip link, keyboard focus styles, responsive layouts, and a print stylesheet are included. All main content works without JavaScript. There are no dummy download buttons or sample publications.
