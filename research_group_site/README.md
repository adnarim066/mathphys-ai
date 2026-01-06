# MathPhys-ai Lab Website

This is the source code for the MathPhys-ai Lab research group website. It is built with clean, semantic HTML5 and CSS3, requiring no build steps or complex frameworks.

## 📁 Project Structure

- `index.html` - Homepage (Hero, Research Highlights).
- `research.html` - Detailed research directions.
- `team.html` - Group members (PI, Postdocs, PhDs, Alumni).
- `publications.html` - List of papers.
- `software.html` - Software tools and datasets.
- `style.css` - Global styles, design tokens (colors, fonts), and layout.
- `assets/images/` - Directory for team member photos.

## 🛠️ Maintenance Guide

### Adding a Team Member
1.  Save their photo (square crop recommended) to `assets/images/filename.jpg`.
2.  Open `team.html`.
3.  Copy an existing member card block:
    ```html
    <div class="card team-card">
        <div class="member-photo" style="background-image: url('assets/images/filename.jpg');"></div>
        <h3 class="card-title">Name</h3>
        <h4 class="card-subtitle">Position</h4>
        <p class="card-text">Research Topic</p>
    </div>
    ```
4.  Paste it into the correct section (Postdoc/PhD/Undergrad) in alphabetical order.

### Adding a Publication
1.  Open `publications.html`.
2.  Copy the top-most `.pub-item` block.
3.  Update the **Title**, **Authors**, **Tag** (e.g., "Math Phys"), **Year**, and **Journal/ArXiv** info.
    ```html
    <div class="pub-item">
        <div class="pub-title">Paper Title</div>
        <div class="pub-authors">Authors List</div>
        <div class="pub-meta">
            <span class="pub-tag">Math Phys</span>
            <span>2026</span>
            <span>arXiv:xxxx.xxxxx</span>
        </div>
    </div>
    ```

## 🚀 Deployment (GitHub Pages)

This site is optimized for **GitHub Pages**.

1.  **Upload Code**: Push this entire folder to a new GitHub repository (e.g., `mathphys-site`).
2.  **Enable Pages**:
    *   Go to **Settings** > **Pages**.
    *   Under "Source", select `main` branch.
    *   Click **Save**.
3.  **Done!** Your site will be live at `username.github.io/mathphys-site`.

### 🌐 Using a Custom Domain (e.g., mathphys.ai)

Yes, you can use a custom domain!

1.  **Buy Domain**: Purchase your domain (e.g., `mathphys.ai`) from a registrar (Namecheap, GoDaddy, Google Domains, etc.).
2.  **Configure GitHub**:
    *   Go to Repository **Settings** > **Pages**.
    *   Under **Custom domain**, type `mathphys.ai` and click **Save**.
    *   This will automatically create a `CNAME` file in your repository.
3.  **Configure DNS** (at your registrar):
    *   Add `A` records pointing to GitHub's IPs (check GitHub docs for current IPs).
    *   Add a `CNAME` record for `www` pointing to `username.github.io`.
4.  **HTTPS**: Check the "Enforce HTTPS" box in GitHub settings (it may take up to 24h to become available).

## 🎨 Design Notes

- **Colors**: Defined in `style.css` under `:root`.
    - Accent Blue: `var(--color-accent)` (#0E1F8C) (used for lines, buttons, links).
    - Text Grey: `var(--color-primary)` (#464A4E).
- **Typography**: Uses 'Inter' for body text and 'Outfit' for headings.
