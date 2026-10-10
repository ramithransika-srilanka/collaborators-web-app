# Collaborators web app (desktop)

Desktop web app for collaborators on the UGC Platform. Open `index.html` in a browser — no build step needed.
It uses the same top menu, design tokens and components as the brand web app.

## Pages

- **Invites** — brands inviting you to collaborate on their campaigns. Each invite card shows the brand,
  industry, when it was posted, the start date, project tags and a short brief, with a live "Closes in …"
  countdown underneath. Invites closing soonest come first. **Start Chat** and **✕** take an invite off the
  list (both can be undone from the toast). Header search (`/` to open, `Esc` to close) filters by brand;
  the bell opens the notifications popover.

## Assets

`assets.js` holds the brand logos and header icons shared with the brand web app. It is generated, not edited by hand:

```sh
node scripts/sync-assets.js <path-to-brand-web-app>
```
