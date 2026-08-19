# Changelog

All notable changes to Lexo. Every version is signed and notarized by Apple and
distributed from [Releases](https://github.com/Titi257/lexo/releases/latest);
Lexo 1.2.0 and later update themselves.

## 1.2.3

- 🛡 **One instance at a time** — launching Lexo while it is already running (from
  the mounted DMG, say, while the installed copy is active) now cleanly replaces
  the old instance instead of coexisting with it. Two simultaneous instances
  competed for the clipboard, so the shortcut could "translate" previously copied
  content instead of your selection.

## 1.2.2

- 🌍 **Unsupported languages are clearly flagged** — selecting text in a language
  Apple Translation does not cover (Hungarian, Czech, Greek, Swedish…) now shows
  "Language not supported", naming the detected language, instead of an
  unreadable mistranslation.
- 🎯 **Sharper language detection** — a close language is only picked when it is
  genuinely plausible; detection never forces a wrong guess.
- 💬 The new message is localized in all 40 interface languages.

## 1.2.1

- 🛠 **More reliable language detection** — the detected source language is now
  always one Apple Translation can actually handle (Russian is no longer mistaken
  for Kazakh, for instance). No more unwarranted "Translation failed".
- 💬 **Clearer error messages** — when a language pair really is unsupported,
  Lexo explains precisely why instead of showing "Translation unavailable".

## 1.2.0

- 🌍 **Interface in 40 languages** — Lexo follows your Mac's language
  automatically (German, Spanish, Japanese, Arabic…).
- 🔤 **Manual interface language** picker in Preferences, applied instantly, no
  restart.
- 📦 **Models tab** — the full list of supported languages, with a "Download all"
  button.
- 🔄 **Automatic updates** built in: from this version on, updates install in one
  click.
