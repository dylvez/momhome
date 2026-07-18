# Setting up Susie's laptop

Her home page lives at: **https://dylvez.github.io/momhome/**

## 1. Point Chrome at it

1. In Chrome: **Settings → On startup → Open a specific page** → add
   `https://dylvez.github.io/momhome/`.
2. Optional: also set it as the **Home button** page (Settings → Appearance →
   Show home button) so one click always brings her back.

Since Chrome already launches at startup, she'll land on this page every
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

If she uses Office Online instead of desktop Office, use
`https://office.com/launch/word`.

## 3. Windows tweaks (10 minutes, big payoff)

- **Auto sign-in**: run `netplwiz`, select her account, uncheck
  "Users must enter a user name and password". No password screen to get stuck on.
- **Clean taskbar**: unpin everything except Chrome (and Word if you like).
  Fewer icons = fewer wrong turns.
- **Clean desktop**: remove all icons, or everything except a Chrome shortcut.
- **Text size**: Settings → Accessibility → Text size → ~125%.
- **Notifications off**: Settings → System → Notifications → off. No scary popups.
- **Mouse pointer**: Settings → Accessibility → Mouse pointer → bigger, black.

## 4. Updating her page (from anywhere)

Everything editable — her name, the footer note, the buttons — lives in
[config.js](config.js). To change something:

```sh
# edit config.js, then:
git add config.js && git commit -m "update tiles" && git push
```

GitHub Pages redeploys automatically in under a minute. Next time her page
loads, the changes are live. No touching her laptop.
