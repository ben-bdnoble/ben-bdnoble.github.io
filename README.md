# ben-bdnoble.github.io

## Updating The Site

Edit `site-config.js` for settings that change over time. No build step is needed.

- `releaseText`: Updates the release message near the book title and newsletter. Set it to `""` to hide both.
- `bookCover.src`: Filename or path of the book cover, for example `"cover-2027.jpg"`.
- `familyPhoto.src`: Filename or path of the family photo, for example `"family-new.jpg"`.
- Each image's `alt`: A plain-text description for screen readers.
- `announcement.enabled`: Set to `true` to show a message between the title and navigation in the sticky header, or `false` to hide it. On mobile it is right-aligned beside the title, with the menu below. It stays visible as visitors scroll.
- `announcement.text`: The announcement message. Plain text only; an empty message stays hidden even when enabled.

Upload new images alongside `index.html` (or into a subfolder) and use their exact,
case-sensitive paths in the config. The cover stays at most 280px wide and the
family photo at most 220px wide; both keep their original proportions.

For example, to show an announcement, change its settings to:

```js
announcement: {
  enabled: true,
  text: "The Rebel of Machrinath is coming in 2027. Sign up for release alerts!"
}
```

Keep quotes around text and image paths, and use unquoted `true` / `false` values.
Publish the updated config and new images with the rest of the site. Settings
apply when the page loads, including when opening `index.html` locally. JavaScript
must be enabled for the release message and announcement; the images in the HTML
remain available without it.
