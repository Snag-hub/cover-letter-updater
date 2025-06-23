# Cover Letter Updater

A static webpage that generates customized cover letters as PDFs, built with React, Tailwind CSS, markdown-it, and jsPDF. Deployed on GitHub Pages with automated CI/CD.

## Features

- Input fields for company name and position.
- Dynamic date insertion (e.g., "June 23, 2025").
- Markdown template (`cover_letter.md`) with placeholders (`{{company}}`, `{{position}}`, `{{date}}`).
- PDF generation with:
  - A4 size, 25mm margins, 12pt font, 5mm line spacing.
  - Justified text for near-full-width lines (80% of max width).
  - Roboto font with Times fallback.
- Hosted on GitHub Pages.

## Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/Snag-hub/coverletter-updater.git
   cd coverletter-updater
   ```
2. **Install Local Server (Optional)**:
   ```bash
   npm install -g serve
   ```
3. **Run Locally**:
   ```bash
   serve
   ```
   Open `http://localhost:3000`.
4. **Test**:
   - Enter a company name and position.
   - Click "Update & Download PDF" to verify PDF output.

## Deployment

1. **Push Changes**:
   ```bash
   git add .
   git commit -m "Update site"
   git push origin main
   ```
2. **GitHub Actions**:
   - Pushes to `main` trigger automatic deployment.
   - Check Actions tab for build status.
3. **Access Site**:
   - Visit `https://Snag-hub.github.io/coverletter-updater`.

## Customization

- **Edit Cover Letter**:
  - Modify `cover_letter.md` and push changes.
- **Change Font**:
  - Update font URL in `index.html`.
- **Adjust Justification**:
  - Edit `justificationThreshold` in `index.html`.

## Troubleshooting

- **404 Error**: Ensure `index.html` and `cover_letter.md` are in the root and GitHub Pages is set to `main` branch, `/ (root)`.
- **Font Issues**: Check console for CORS errors; consider base64 font.
- **Markdown Not Loading**: Verify `cover_letter.md` path (`./cover_letter.md`).

## License

MIT License
