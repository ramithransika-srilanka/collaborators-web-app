# Collaborators web app (desktop)

Desktop web app for collaborators on the UGC Platform. Open `index.html` in a browser — no build step needed.
It uses the same top menu, design tokens and components as the brand web app.

## Pages

- **Invites** — brands inviting you to collaborate on their campaigns. A dark bar under the top menu switches
  between Open, Chatting and Declined invites (`#/open`, `#/chatting`, `#/declined`). Each invite card shows the
  brand, industry, when it was posted, the start date, project tags and a short brief, with a live
  "Closes in …" countdown underneath. **Start Chat** moves an invite to Chatting, **✕** declines it
  (both can be undone from the toast), and declined invites can be restored while still open.
  Header search (`/` to open, `Esc` to close) filters by brand; the bell opens the notifications popover.

## Assets

`assets.js` holds the brand logos and header icons shared with the brand web app. It is generated, not edited by hand:

```sh
node scripts/sync-assets.js <path-to-brand-web-app>
```
