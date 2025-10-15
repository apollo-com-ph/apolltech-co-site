# GitHub Pages Deployment for Hugo

This site is built with [Hugo](https://gohugo.io/) using the [Profile theme](https://themes.gohugo.io/themes/hugo-profile/).

## Custom Domain
- The custom domain is set to: **apollotech.co**
- The `static/CNAME` file is included for GitHub Pages custom domain support.

## Deployment Steps

1. **Build the site:**
   ```bash
   hugo
   ```
   This generates the static site in the `public/` directory.

2. **Push to GitHub Pages branch:**
   - For user/organization sites, push the contents of `public/` to the `main` branch.
   - For project sites, push to the `gh-pages` branch.

   Example for project site:
   ```bash
   hugo
   git add .
   git commit -m "Build site"
   git subtree push --prefix public origin gh-pages
   ```

3. **GitHub Pages Settings:**
   - In your repository settings, set the Pages source to the correct branch (`main` or `gh-pages`) and `/ (root)`.
   - Ensure the custom domain is set to `apollotech.co` in the Pages settings.

## Local Development

To serve the site locally:
```bash
hugo server
```

---

For more details, see the [Hugo documentation](https://gohugo.io/hosting-and-deployment/hosting-on-github/).
