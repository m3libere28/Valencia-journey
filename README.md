# Valencia Journey

A beautiful, single-file static site that serves as a family transition guide for moving to Valencia, Spain. It includes:

- Welcome, Timeline, Documents (DNV), Budget, Schools, Oakland Property, and Logistics tabs
- Interactive budget editor (with live USD→EUR conversions)
- Google Maps integration for schools (requires your own API key)

## Local Development

Just open `index.html` in your browser.

## Google Maps API Key

Replace `YOUR_API_KEY` at the bottom of `index.html` with a valid Google Maps JavaScript API key. You can obtain a key here:
https://developers.google.com/maps/documentation/javascript/get-api-key

Then restrict the key by HTTP referrer to your GitHub Pages domain after deployment.

## Deploy on GitHub Pages

1. Create a repository in your GitHub account (e.g., `valencia-journey`).
2. Push this folder's contents to that repository's `main` branch.
3. In the repo, go to `Settings` → `Pages` → `Build and deployment`.
   - Source: `Deploy from a branch`
   - Branch: `main` and `/ (root)`
4. Your site will be available at: `https://<your-username>.github.io/valencia-journey/`

Alternatively, you can use the GitHub CLI:

```
# from the project directory
# create the repo and push in one go (requires GitHub CLI `gh` and you to be logged in)
gh repo create valencia-journey --public --source . --push
```

If you use a custom domain, create a `CNAME` file at the project root with your domain name and add a DNS CNAME record pointing to `<your-username>.github.io`.
