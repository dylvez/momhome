# Setting up Susie's laptop

## 1. Put the home page on her laptop

1. Copy `index.html` somewhere permanent, e.g. `C:\Users\<her-user>\momhome\index.html`.
   (Don't leave it in Downloads — it could get cleaned up.)
2. In Chrome: **Settings → On startup → Open a specific page** → add
   `file:///C:/Users/<her-user>/momhome/index.html`.
3. Optional: also set it as the **Home button** page (Settings → Appearance →
   Show home button) so one click always brings her back.

Since Chrome already launches at startup, she'll now land on this page every
time she turns on the laptop.

## 2. The Word button

The "Write in Word" tile uses the `ms-word:` link, which needs desktop Office
installed. The **first time** she (or you) clicks it, Chrome will ask
"Open Microsoft Word?" — check **"Always allow"** so she's never asked again.

If she always works on the same few documents, an even better option is to
point the tile straight at a document, e.g.:

```
url: "ms-word:ofe|u|file:///C:/Users/<her-user>/Documents/Letters.docx"
```

## 3. Windows tweaks (10 minutes, big payoff)

- **Auto sign-in**: run `netplwiz`, select her account, uncheck
  "Users must enter a user name and password". No password screen to get stuck on.
- **Clean taskbar**: unpin everything except Chrome (and Word if you like).
  Fewer icons = fewer wrong turns.
- **Clean desktop**: remove all icons, or everything except a Chrome shortcut.
- **Text size**: Settings → Accessibility → Text size → ~125%.
- **Notifications off**: Settings → System → Notifications → off. No scary popups.
- **Mouse pointer**: Settings → Accessibility → Mouse pointer → bigger, black.

## 4. Changing the page later

Everything editable lives in one block at the top of the `<script>` section in
`index.html`: her name, the footer note, and the `TILES` list (label, hint,
emoji, link, colors). Edit, save, done — changes show next time the page loads.
