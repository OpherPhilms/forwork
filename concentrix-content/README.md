# Reference Library

A minimal static audio player. No dependencies, no build step.

## File structure

```
concentrix-content/
├── index.html
├── README.md
└── files/
    ├── matt-damon.mp3
    ├── mindy-kaling.mp3
    └── harry-potter.mp3
```

## Adding MP3 files

1. Drop your `.mp3` files into the `files/` folder.
2. Open `index.html` and find the `<ul id="playlist">` section near the bottom.
3. Add a new `<li>` for each file, following the same pattern:

```html
<li>
  <button data-src="files/your-file.mp3">
    Display Name
  </button>
</li>
```

The `data-src` attribute must match the filename exactly (case-sensitive).

## Changing the default track

The player loads `files/matt-damon.mp3` on page open. To change that, update two spots in `index.html`:

- The `<source src="...">` tag inside `<audio>`
- The first `<button>` in the playlist (set `data-src` to match, and keep the `class="active"`)

## Deploy to Netlify (drag-and-drop)

1. Go to [netlify.com](https://netlify.com) and log in (or create a free account).
2. From your dashboard, scroll to the bottom — you'll see a drop zone that says **"Want to deploy a new site without connecting to Git? Drag and drop your site folder here."**
3. Drag the entire `concentrix-content` folder (this folder) onto that drop zone.
4. Netlify deploys it instantly and gives you a live URL.

To update the site later, drag and drop the folder again onto the same site in your Netlify dashboard — it will publish a new version.
