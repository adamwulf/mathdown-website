# Public website for the MathDown editor app

## Development

[Install Hugo](https://gohugo.io/getting-started/installing/) e.g. `brew install hugo`

Live-reloading dev server:

    $ hugo server

And then http://localhost:1313/

## Deployment

Develop on feature branches, pushing freely to Github and using Netlify deploy previews to see results.

`main` branch is a staging / release candidate area.

When ready to deploy, merge changes to the `production` branch and push to GitHub. [The Netlify dashboard for muse-website](https://app.netlify.com/sites/muse-website/overview) shows deploy status.

## Infrastructure notes

* Netlify deploys the `production` branch from GitHub
* DNS by Netlify and SSL by Let's Encrypt via Netlify
* Visitor counting with [Fathom](https://museapp.usesfathom.com/#/?grouping=daily&period=1w)
* Signup talks to Muse API (prod = `api.museapp.com`, dev = `muse-api-dev.herokuapp.com`)

## File Structure Descriptions

Notes from https://kinsta.com/blog/hugo-static-site/

* content
    * The content folder is where your actual post content goes in Markdown or HTML.
    * Hugo treats each top-level directory in the content folder as a content section. Content sections in Hugo are similar to custom post types in WordPress.
* layouts
    * The layouts folder contains template HTML files that define the structure of your site.
    * Hugo templates consist of base HTML with additional dynamic templating powered by Golang’s built-in html/template and text/template libraries.
* static
    * Hugo’s static folder is where you store static assets that don’t require any additional processing.
    * all files in the static folder are copied as-is.

The following folders are created during `hugo` or `hugo server`

* public
* resources


