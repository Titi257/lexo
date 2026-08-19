# Privacy — what Lexo does, precisely

Lexo is a menu bar app that translates the text you have selected. This page
documents exactly what it reads, what it stores, and every connection it makes.
It is deliberately specific: "100% local" is a claim you should be able to check.

## What Lexo reads

When you press the shortcut, Lexo synthesizes a **⌘C** keystroke in the frontmost
app, reads the text that lands on the pasteboard, and immediately restores your
previous clipboard content. That is the only way it ever obtains text.

This is why macOS **Accessibility** permission is required: synthesizing a
keystroke is a privileged operation. Lexo uses it for nothing else — it does not
read your screen, log your keystrokes, or watch other apps.

## Where your text goes

Into `Translation.framework`, Apple's **on-device** translation engine, and back
into the bubble. It is not sent to Lexo, to any server, or to any third party.
There is no account, no sign-in, and no analytics or crash-reporting SDK in the
app.

## What is stored on your Mac

| What | Where | Notes |
|---|---|---|
| Translation history | `~/Library/Application Support/com.kevboileux.translate/history.json` | Last 500 entries. Clear it anytime from **Preferences → History → Clear all**, or delete the file. |
| Preferences | `~/Library/Preferences/com.kevboileux.translate.plist` | Target language, shortcut, interface language. |
| Diagnostic log | `~/Library/Logs/Translate/translate.log` | **Off by default** — a normal install never creates it. When enabled for debugging it records only metadata (text *lengths*, language codes, app bundle ids), never the text itself. |

Nothing here leaves your Mac. Uninstalling is dragging the app to the Trash;
the three paths above are all it leaves behind.

## Every network connection, exhaustively

Lexo itself makes exactly **one** kind of request, and macOS makes one more on
its behalf:

1. **Translation model download — by macOS, not by Lexo.** The first time you use
   a given language pair, macOS downloads the corresponding model (~30 MB) from
   Apple. This is the system's own download flow; Lexo never sees it and your
   text is not part of it. Afterwards, translation is fully offline. You can
   pre-download models in **Preferences → Models**.
2. **Update check — by Lexo, via [Sparkle](https://sparkle-project.org).** Once a
   day, Lexo fetches
   [`appcast.xml`](https://raw.githubusercontent.com/Titi257/lexo/main/appcast.xml)
   from GitHub to see whether a newer version exists, and downloads the `.dmg`
   from GitHub if you accept an update. The request carries no identifier of you.
   **Turn it off** in **Preferences → About → Check automatically**; Lexo then
   makes no network requests at all.

There is no third connection. No telemetry, no usage statistics, no "anonymous"
ping, no ads, no ad SDK.

## How to verify it yourself

Point a network monitor such as [LuLu](https://objective-see.org/products/lulu.html)
(free, open source) or Little Snitch at Lexo, turn the update check off, and
translate all day: you will see nothing. Leave the update check on and you will
see one connection to `raw.githubusercontent.com` per day, and nothing else.

Every release is signed with an Apple Developer ID and notarized by Apple, so
macOS verifies the binary has not been tampered with before it runs.

## Contact

Questions, or something here that does not match what you observe?
[Open an issue](https://github.com/Titi257/lexo/issues/new/choose) — that is a
bug in this document and it will be fixed.

*Last updated: 2026-08-19 · applies to Lexo 1.2.3 and later.*
