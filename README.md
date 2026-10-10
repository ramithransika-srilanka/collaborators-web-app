# Collaborators web app (desktop)

Desktop web app for collaborators on the UGC Platform. Open `index.html` in a browser — no build step needed.
It uses the same top menu, design tokens and components as the brand web app.

## Pages

The top menu has two sections, **Invites** (mail icon) and **Chats** (chat icon), using the coolicons
"Communication / Mail" and "Communication / Chat_Circle_Dots" icons from the Figma file. On phones the logo and the icon nav are replaced by a hamburger that opens the
same sections in a panel sliding in from the left, like the creator web app's phone menu.

- **Invites** (`#/`) — brands inviting you to collaborate on their campaigns. Each invite card shows the brand,
  industry, when it was posted, the start date, project tags and a short brief, with a live "Closes in …"
  countdown underneath. Invites closing soonest come first. **Start Chat** opens a chat with that brand;
  **✕** declines the invite (undo from the toast). Header search (`/` to open, `Esc` to close) filters by brand;
  the bell opens the notifications popover.
- **Chats** (`#/chats`, `#/chats/<invite>`) — conversations started from invites. The chat list on the left
  shows the latest message, time and an unread dot (also shown on the Chats icon in the top menu); the open
  chat on the right pins the invite it came from, then the messages. `Enter` sends, `Shift+Enter` adds a line.
  The brand side is simulated. When a chat starts from an invite card, the brand sends its opening messages
  one after another as ordinary chat bubbles: a greeting, the campaign summary, any attachments (each file as
  its own message), the total budget, the timeline, and finally asks what commission you expect. After you
  reply it answers after a short "typing…" indicator.
  On phones the list and the open chat show one at a time.

## Assets

`assets.js` holds the brand logos and header icons shared with the brand web app. It is generated, not edited by hand:

```sh
node scripts/sync-assets.js <path-to-brand-web-app>
```
