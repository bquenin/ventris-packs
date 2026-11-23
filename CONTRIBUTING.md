# Contributing a pack or a correction

A pack is plain text, in any language and any alphabet, written with no programming and no hacking of the
game. The packs here now are working samples, machine translated and not reviewed by a human translator,
and anyone is free to improve them or to add a pack of their own.
[Translating a game](https://github.com/bquenin/ventris/blob/main/docs/translating.md) walks through
fixing a line, reviewing a part of a game and starting a pack, with the ventris app, a text editor and the
browser; no terminal is needed. This page is the rules a pack here follows.

## What a pack is

- **Text only.** Script files, `names.txt` where the game has one, `pack.toml`, `NOTES.md`, and other notes.
  No font files: the fonts built into `ventris` draw the letters, and a font a language needs is proposed
  for `ventris` itself.
- **Laid out as `game/language/`**: the game's id as `ventris games` shows it, then the language's IETF tag
  (`en`, `fr`, `pt-BR`, `zh-Hant`).
- **Sparse.** A pack holds only the strings it changes. Strings are named by their address, `section.number`,
  which never changes.

## What `pack.toml` must say

The format is in the engine's [docs/packs.md](https://github.com/bquenin/ventris/blob/main/docs/packs.md).
For a pack here, four things are required besides what the format itself needs:

- **`authors`**: who made it. Add your name when you contribute a substantial part of a pack.
- **How it was made**, in `authors` or `description`: written by hand, machine translated, machine
  translated and then corrected, translated from another pack.
- **What has been seen on screen**, in `description`, in a sentence, with `NOTES.md` giving the detail.
- **`license = "CC-BY-NC-SA-4.0"`**: the licence of every pack here, as [Licence](#licence) says.

## `NOTES.md`

Every pack has one. It holds:

- the names and terms the pack has chosen: characters, places, skills, items, recurring words and phrases;
- how its strings are written: punctuation, capitals, how names and numbers are handled;
- what has been seen on screen, and what has not; and what is still open.

When you look at something on screen, add it here. The next reviewer starts from it.

## Rules

- **Never the game.** No game file, no extracted script, no built image, no patch made from a game, no
  picture of the game's font. A screenshot belongs in an issue or a pull request, not in a pack.
- **Machine translation is allowed, and declared.** A pack may be machine translated in whole or in part,
  as long as its `pack.toml` says so in `authors` or `description`.
- **No copying another translation's text** unless its licence allows it and it is credited in
  `pack.toml`. An existing translation may be used to check facts, such as what a name refers to. A pack
  made from another pack here is under that pack's licence and credits its authors.
- **One pack per game and language.** Improve the pack that is there rather than starting another; propose
  a big change in an issue first.
- **A name is the same everywhere.** Changing an established name means changing it in every file of the
  pack and in `NOTES.md`, in the same pull request.
- **Say what you saw.** In the pull request, say which strings you saw on screen and which you only built
  or did not build. A build that succeeds is not a translation that works: only the screen shows that.
- **Check it builds** where you can: in the app, on the game's **Make a translation** tab, under **Your
  pack**, choose your copy of this repository with **Choose your pack's folder…**, see that the pack is not
  marked **Cannot be used**, and build it into your copy of the game. If you cannot, say so.

## Licence

A pack here is under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International licence
(CC BY-NC-SA 4.0), in [LICENSE](LICENSE), and its `pack.toml` says so with `license = "CC-BY-NC-SA-4.0"`.
The [README](README.md#licence) says in plain words what it allows. By sending a pack or a change, you
agree to share it under that licence, along with the permission the README gives for videos and streams,
and you confirm that the text is yours to give: your own words, or a machine translation you directed, or
text whose licence allows it and which is credited.
