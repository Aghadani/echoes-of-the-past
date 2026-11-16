# Echoes of the Past

A browser based historical portrait mirror. Choose Roman Mosaic, Renaissance, Neon Future, or Golden Dynasty. The visual effect follows your face as you move. Adjust its intensity, flip the mirror, and capture a PNG.

## Publish with GitHub Pages

### 1. Create a repository

1. Sign in at [github.com](https://github.com).
2. Click **+** in the top right, then **New repository**.
3. Enter a repository name, such as `echoes-of-the-past`.
4. Choose **Public** (required for GitHub Pages on GitHub Free) and leave **Add a README file** unchecked.
5. Click **Create repository**.

### 2. Upload the app files

1. In the new repository, choose **Add file → Upload files**.
2. On your computer, open the `outputs` folder from this project.
3. Drag these four files into the upload area: `index.html`, `app.js`, `style.css`, and `README.md`. Make sure they appear at the repository's top level, not inside an `outputs` subfolder.
4. Enter a commit message such as `Add Echoes of the Past app` and click **Commit changes**.

### 3. Turn on GitHub Pages

1. In the repository, open **Settings**.
2. In the left menu, open **Pages** (under **Code and automation**).
3. Under **Build and deployment**, choose **Deploy from a branch** as the source.
4. Choose branch **main** and folder **/(root)**, then click **Save**.
5. Wait a minute, then refresh the Pages settings. GitHub will show the published site link there, usually `https://YOUR-USERNAME.github.io/echoes-of-the-past/`.

### 4. Use the mirror

Open the Pages link in a current browser, click **Enable Camera**, and allow camera access. The model is fetched from online CDNs on first use, so the page needs an internet connection. Camera frames are processed in your browser and are not uploaded.

## Local preview

Camera access requires HTTPS or `localhost`. To preview on your computer, open a terminal in this folder and run:

```bash
python -m http.server 8000
```

Then open http://localhost:8000.

## Notes

- This is a static web app, so GitHub Pages is sufficient; no Python server or Streamlit deployment is needed.
- Effects are a lightweight landmark-driven prototype, not a generative AI model.
- The page loads MediaPipe from jsDelivr, its face landmark model from Google Cloud Storage, and fonts from Google Fonts.
