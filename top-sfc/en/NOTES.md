# Tales of Phantasia in English: translator's notes

This pack is being written as a worked example of translating a whole game with ventris. These
notes hold what a second translator would need to carry on in the same way: how the text is written,
the names that were chosen, and what was learned about the game along the way.

## How the text is written

- **Speakers.** A line of dialogue starts with who speaks, on a line of its own, then what they say.
  A party member is written as their tag (`{クレス}`), which the game replaces with the name from
  `names.txt`. Anyone else is written in plain words (`Maria`, `King of Euclid`, `???`).
- **Speech** is in double quotes. Thoughts are in parentheses. A sign or a book is introduced with
  `It reads:` and quoted.
- **Tags are kept as the game has them.** `{COLOR:..}`, `{SPEED:..}`, `{STR:..}` and `{NUM:..}` stay,
  each as often as in the game's string. `{PAGE}` stays where a new speaker starts. A string that
  ends with `{PAGE}` in the game must end with it in the translation, or the next string runs on in
  the same box. A small script of the author's checked all of this; it is not part of the pack.
- **Do not keep the game's line breaks inside a sentence.** The game's text was laid out by hand for
  Japanese, and a break carried over from it lands mid-sentence in English and leaves a short line.
  Write a paragraph as one line and let the build wrap it. A script can join such breaks, but read
  what it changed: it cannot tell a title from a sentence.
- **Narration set in from the left** with full-width spaces keeps its breaks. Keep each line short,
  about 25 letters, or its last word wraps onto a line of its own.
- **Long speech needs no page breaks.** The box shows the speaker and three lines. When it is full
  the game waits for a button and scrolls, so a long paragraph can be written in one piece.
- **Eight lines are shown as sprites.** The game shows them over the scene with no box, each
  character a sprite, 14 dots apart: `01.004`, `07.000`, `49.079`, `59.008`, `79.053`, and
  `99.000` to `99.002`. The extracted script has a comment under each, and so does this pack.
  Write such a line as any other, with ordinary spaces. The build breaks its rows at 15
  characters. What is left to the translator is the page: it holds 32 letters, spaces not
  counted, and the build refuses a longer one. Put a `{PAGE}` where the page should turn, or say
  it in fewer letters. The Japanese never needs more than 32, so its sentences are shorter here
  than in English: these lines are tighter than a free translation would be (`A lone bridge joins
  it to the mainland.`), and three of them take one page more than the game's own.
  How each is drawn has been seen by putting its text in the place of `01.004`, which is a minute
  from a saved state. Only
  `01.004` has been seen in its own scene; where on the screen the others sit there has not.
- **Place names hold 16 characters.** The name of a place or a shop, shown in a box at the top of
  the screen when you enter it, is one of 122 strings the game centres by counting their characters.
  It holds 16; a party member's name counts as its letters and one more. A longer one is not drawn
  at all: the box shows what was left of the message before it. So these names are short, without
  quotes, the shop's name before what it sells (`Teasel Weapons`, `Gori's Store`), and a place can
  be named more shortly here than in a sentence (`Spirit Forest` in the box, the Forest of Spirits
  when someone speaks of it). Version 0.9 had 69 of them too long; 0.9.1 shortens those and leaves
  alone the ones that already fitted, which is why some shop names still carry quotes
  (`Item Shop "Draw"`).
- **Comments.** A line that starts with `# ` is a comment, in any script file. Use them for what
  the next translator should know about one string: why it is worded as it is, what it must agree
  with elsewhere.
- **Sentences split over strings.** Now and then the game ends a sentence in one string and puts its
  full stop in the next (`21.011` and `21.012`). The translation does the same: the first string has
  no final stop and no closing quote, and the second is `."`.
- **Menus are in capitals and small letters.** The menu font has capitals, digits and
  `- . , ! ? & : / + = ( ) < > ~`, and 192 tiles in all. The build gives a new character the tile
  of a kana that no menu string uses any more, and the small letters and the apostrophe need 27.
  With the menus in English, one thing still used the kana: the letter grid of the naming screen
  (strings 670 and 711 to 755). So this pack puts `A` to `Z` and `a` to `z` in that grid, which
  frees the tiles. That is all it does to the naming screen, and it is an exception made for this
  game. A pack that leaves the grid as it is has one spare tile, and its menus are in capitals.
- **The naming screen is not translated.** A player keeps the names the pack gives. Whoever opens
  the screen (from the status screen, on the name) leaves it with B, and the name stays.
- **A menu string can also be drawn large.** The name of the item being described, above its
  description, is the menu string drawn in the captions' font, one letter to a cell: `A p p l e G u m`.
  The build gives the captions' font a full-width glyph for each letter the menu font gained and
  says how many.
- **Menu strings are fitted to their columns.** The menus draw a string in a column of fixed width
  and do nothing for one that is longer: the item list cuts a name at 8 characters, a label runs
  into the one beside it, an option word runs off the box. The game's own strings show the widths:
  8 for the name of an item, a piece of equipment, a spell, a monster or a title; 12 for a sword
  skill; 4 for an equipment slot; 3 where an icon follows. So the Apple Gummy is `AppleGum` and the
  Long Sword `LongSwrd`: where words are run together, each keeps its capital, which is what makes
  them readable. `MENU-NAMES.md` lists every shortened string and what it stands for. A name
  of 8 characters also leaves room for the word that says what kind of item it is, which a longer
  name pushes out of the description box.
- **One string can be on two screens.** The narrower place decides. `Gear` is the main menu's label
  and the heading of the equipment screen's first column, five characters from the next.
- **Where the width cannot be had, a label can be moved.** `Skills` is the main menu's first label
  and also labels a row of the status screen, where the game draws a picture of the control pad
  right after its third letter. The word was `Skl` for that reason. A pack can now move the
  menus' fixed labels, in `pack.toml` under `[layout]`, and this one moves the right-hand column
  of the status screen two columns to the left and the picture one to the right, which is what
  the DeJap translation did. The extracted `menu.txt` names each place a string is drawn at, in a
  comment under the string. What is beside a label does not move with it, so each move has to be
  looked at on the screen. Move a label only where no wording fits.
- **Names** are set twice, and must agree: in `names.txt` for dialogue and in `menu.txt` for the
  menus (`Cress`, strings 414 to 420).
- **The sign between a given name and a family name** (`Cress = Albane` on the status screen) is
  replaced by a space: string 759 is a space, and `pack.toml` moves the family name over it.

## Names and terms

| Japanese | English |
| --- | --- |
| クレス, ミント, アーチェ, チェスター, クラース | Cress, Mint, Arche, Chester, Claus |
| アルベイン, アドネード, クライン, バークライト | Albane, Adnade, Klein, Barklight |
| ダオス, モリスン, デミテル | Dhaos, Morrison, Demitel |
| ミゲール, マリア, アミィ, トリスタン | Miguel, Maria, Ami, Tristan |
| オルソン, ジョアン, マルス | Olson, Joan, Mars |
| レニオス, ハリソン, スタンリー | Lenios, Harrison, Stanley |
| すず, 銅蔵, おきよ | Suzu, Dozo, Okiyo |
| トーティス, ユークリッド, ベルアダム | Toltus, Euclid, Belladam |
| アルヴァニスタ, ベネツィア, ミッドガルズ | Alvanista, Venezia, Midgards |
| モーリア坑道, トレントの森, ローン島 | Moria Mine, Treant's Forest, Lone Island |
| 精霊の洞窟, 忍者の里 | Cave of Spirits, the ninja village |
| ユグドラシル, マーテル, ヴォルト | Yggdrasil, Martel, Volt |
| レアバード | Rheaird |
| 法術 | healing arts |
| 魔術, 魔法 | magic |
| 魔科学 | magitech |
| 記憶陣 | memory circle |
| 時間の剣 | Sword of Time |
| 独立騎士団 | the Independent Knights |
| 天下一武術大会 | the Grand Martial Arts Tournament |
| リア・スカーレット, メイアー, レアード | Rhea Scarlet, Meyer, Laird |
| ルーングロム (グロム), エドワード, リリス | Lundgrom (Grom), Edward, Lilith |
| ジャミル, ジェストーナ, イシュラント | Jamir, Jestona, Ishlant |
| ライゼン, ブラムバルド, 乱蔵 | Raizen, Brambert, Ranzo |
| アイフリード, グラハム | Aifread, Graham |
| ヴァルキリー, フラムベルク, フェンビースト | Valkyrie, Flamberge, Fenbeast |
| ウンディーネ, イフリート, ノーム, シルフ | Undine, Ifrit, Gnome, Sylph |
| マクスウェル, ルナ, アスカ, シャドウ, オリジン | Maxwell, Luna, Aska, Shadow, Origin |
| アルテミス, ペガサス, ユニコーン | Artemis, Pegasus, Unicorn |
| ハーメル, フレイランド, オリーブヴィレッジ | Hamel, Freyland, Olive Village |
| フリーズキール, アーリィ, ミゲール | Friezkiel, Arlee, Miguel |
| ヘイムダール, トール, オーディーン, フェンリル | Heimdall, Thor, Odin, Fenrir |
| 水鏡ユミルの森, 白樺の森, 精霊の森 | Forest of Ymir on the Mirror Lake, White Birch Forest, Forest of Spirits |
| １２星座の塔, 炎の塔, 氷の洞窟 | Tower of the Zodiac, Tower of Flame, Cave of Ice |
| 熱砂の洞窟, 浸食洞, 闇の洞窟 | Cave of Burning Sand, Sea Cave, Cave of Darkness |
| ヴァルハラ平原, デリス・カーラーン | Valhalla Plains, Derris-Kharlan |
| 超古代文明 | the far ancient civilisation |
| 魔科学兵器, 魔法研究所 | magitech weapon, magic laboratory |
| 契約の指輪, 召喚 | pact ring, summon |
| 奥義書, 呪文書, 魔術書 | book of secret arts, spellbook, grimoire |
| 三種の武具, 大いなる実り | the three arms, the Great Seed |
| 冒険者ギルド, 交易品 | Adventurers' Guild, trade goods |
| 秘密の言葉, 決定 | secret word, confirm |
| ガルド | Gald |
| グミ | Gummy |
| アセリア暦 | the Aselian calendar |

Sword skills are written in the game as the sound of their names, so they are given as that sound in
Latin letters (`Majinken`), the same in the menus, in the captions and in a sentence.

## What the game does with a translation

- An area's dialogue in English is often larger than the memory the game has for it. The build then
  keeps that area's dialogue on the cartridge and says so (`cartridge:` and the areas). Nothing has to
  be done about it.
- The game has a third body of text, which `ventris extract` writes as `captions.txt`: what a
  battle says, the names of skills in kanji, the descriptions of items, and the headings and messages
  of the menu screens, 622 strings in all. How they are written is below.

## How the captions are written

The game draws a caption in cells 16 dots wide and does nothing else for it: it does not wrap a
line, and it gives a caption no more room than the game's own took. The build puts two letters in
a cell. Everything here follows from that.

- **Thirty letters to a line, two lines to a description.** A longer line runs off the box and
  scrambles the heading above it. Break every line yourself.
- **Pieces.** A description is often several captions joined: `{PHRASE:EA62}` is caption 81, shown in
  that place. Japanese order is kept by the game, so the pieces are cut to read in English in that
  order: `A small jelly,` then ` apple flavour.` and a new line, then `HP` then ` +30% of max`.
  `captions_tool.py phrases` in the engine's repository lists each piece and what uses it.
- **Even numbers.** A cell is not shared between pieces. A piece that another follows on the same
  line needs an even number of letters, or a gap shows. A space at the end of the piece or the start
  of the next one is the usual way to get there (`War god ` with its space is eight).
- **Pieces left empty.** Where English cannot put the changing word first, the caption says the whole
  sentence and no longer calls the piece: captions 96, 107 and 428 are empty for that reason.
- **Headings keep to the game's width.** `特技` is two cells, so the heading is four letters: `Tech`.
  A longer one overwrote the text beside it. That is why the headings are `Gear`, `Tech`, `Plan`,
  `Line` and `Arts`, though the main menu, which has its own font and its own strings, says
  `Skills`, `Tactic` and `Lineup`.
- **Blank cells for pictures.** Where the game draws a button over the text, the caption has the
  game's wide space in that cell. They are kept, one for one.
- **Skill names** are the sound of the name, as in the menus, in ordinary letters: `Majinken`. The
  battle shows them in a field of ten cells, so up to twenty letters.
- **What a number or a name is joined to** starts with a space: ` Gald gained!`, ` levels up!`.
- **A caption's own last line break is kept.** Ten of the game's captions end in one (79, 85, 95,
  210, 221, 226, 238, 255, 290, 558). In the file that is one more blank line.
- **The song's credits** (603 to 611, 615) are the names of its makers and singers, written in
  Latin letters, family name last, and the song's title in English.

`captions_tool.py check` lays every caption out as the game will and names a line that is too long
and a gap between pieces. It names one: caption 534, at 19 cells, which is shown in a wider box
(the game's own line there is 22). The build then lists the captions that take more cells than
the game's own. Most of those are descriptions, whose box always has two full lines; the ones to
look at on screen are short labels.

- **Sentences the game assembles from pieces.** Some sentences are several strings shown one after
  another: a fixed start, one of a few middles, a fixed end (`53.002` to `53.006`, `67.034` to
  `67.039`, `95.001` to `95.006`). Japanese puts the changing word first and the verb last; English
  wants the verb first. So the pieces are cut differently: `Received {STR:..}` in each of the middles
  and a bare `.` in the end piece. A piece that follows another on the same line starts with a space.
  Read the neighbouring strings before translating a string that looks like a fragment.
- **A lone full stop is a string.** Where the game has `。` as a string of its own, the sentence
  before it was left open on purpose because another string may follow instead. The translation keeps
  the same cut: the sentence without its stop, then `."`.
- **Names in a sentence come from the menu.** An item or a spell named through `{STR:..}` is whatever
  `menu.txt` calls it. Where a sentence names a skill or a title in plain words, use the spelling in
  `menu.txt` (`Hououtenkuuha`, `Sword Master`), or the two will disagree on screen.

## Where it stands

Every string of dialogue (3,201 in 50 files), the menu strings, the names and 614 of the 622
captions are translated; the other 8 are empty or only point at another caption. `check.py` passes
on the dialogue, and `captions_tool.py check` names the one caption said above.

Looked at in an emulator, with the menus in capitals and small letters: the main menu and the
item, skills, equipment, status, tactic, lineup and custom screens, with one item and no skills,
and the status screen again with its column moved; the naming screen, to see that B leaves it
with the name kept; and battles on the world map and in the forest, with the party's and the
monsters' names in their boxes, `24 Gald gained!` and `Chester levels up!` in the bar at the end.
Not seen: a skill's name in battle, the status word `Poison` (three cells where the game has
one), shops, the song's credits, a name typed on the naming screen, and any menu list long
enough to show more than a few of the shortened names.

A tactic name on the status screen has 13 columns, the most the game clears when the page turns
(a longer trial name left its end behind): `Normal attack` fits, leaves nothing on the next page, and
sits inside its box on the Tactic screen, which has room for 18. No saved state reaches the fifth
member, so `F. Lester` was seen in place of Cress's family name in a scratch build: `Cress F. Lester`.

The place names as 0.9.1 shortened them: `Teasel Weapons` was seen on walking into the weapon shop
in Toltus, `St Lenios Church` and `Gori's Store` in the place of `05.000` (Cress's house) in a
scratch build, and `Toltus Village`, which already fitted, on entering the village. Each was drawn
whole, and the box closed. The other place names have not been seen.

Of the dialogue, only the opening scene, the hunt in the forest south of Toltus and one long
passage have been looked at, and the eight lines shown as sprites as said above.
Everything else is built and checked by the program but not seen, so expect small faults: a line a
little too long for the box, a quote mark left open where two strings meet, a name a later scene
shows to be wrong. The places most worth looking at are the sentences assembled from pieces, the
indented narration, and the numbered choices.
