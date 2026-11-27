# Ganbare Goemon DS in English: translator's notes

Ganbare Goemon: Tōkai Dōchū Ōedo Tengurigaeshi no Maki (Konami, Nintendo DS, 2005). This pack is machine
translated, directed by bquenin, and not reviewed by a human translator. These notes hold what a second
translator needs to carry on in the same way.

## How the text is written

- **No line breaks of the game's own inside a sentence.** The Japanese was broken by hand at 10
  characters a line. The build breaks lines at spaces: 20 letters a line in dialogue, 28 in the
  system's messages. Write a string as one paragraph.
- **A new box**: `{0D}{0A}` makes the game wait for a button and clear the box. It stays where the
  game has it, between the same two thoughts. A box shows three lines; past that the game waits and
  clears by itself, so a long string needs no breaks of its own.
- **Readings** (`{RUBY:000N}…{RUBY_END}`, the furigana) are left out.
- **Other tags stay** where they fall in the sentence: `{WAIT:…}` (a pause, in frames), `{07:…}` (the
  speaker's look changes), `{5B:…}` (colour).
- **Speakers** are not written: the game shows the speaker's face and a name plate, which is a picture.
- **Punctuation**: English quotes and punctuation; `・・・` is an ellipsis, `...`.
- **No macrons**: Tokaido, Kinemon, Tokutaro. The game's names are written as they are spoken.
- **Units and money**: 両 and 小判 are ryo, as the series' English releases have it; 里 (distance) is ri.
- **The storyteller** (`stage_demo`) narrates in a showman's rhythm, short lines that rhyme or nearly so in
  Japanese. The English keeps a storyteller's voice and short lines; the pack turns on the build option
  `horizontal-storyteller`, which writes those pages across, 12 letters a line, left page first.
  Its strings are laid out by three rules, which a small script of the author's applied:
  - A string that opens a quote (﹁ in the Japanese) is where the speaker's small face is drawn, over
    about three cells at the start of the line. It starts with two spaces, and its first line holds
    at most 9 cells, the spaces included: a manual break goes after the first word or two.
  - A string the game runs on into the next, with no line break between (01832, 03086, 04416, 06306,
    07714, 09120, 11260, 11576, 15214, 17240, 19946), ends with a line break of its own, so that the
    next starts on a new line; otherwise the game breaks the joined line in the middle of a word.
  - The exception is 16654 ("For / some reason,"): after it the script starts the next speaker's turn
    in an odd order, and a longer first line, or a line break at its end, stops the game there.
    It keeps its first line short and runs on into 16706.
  - The two sound effects (15070, 18958) are in quotes in the Japanese but have no face, and no indent.

## Voices

- **Goemon**: rough, quick, Edo street talk. Calls Ebisumaru "you" or by name; てやんでい is
  "Get outta here!" or a short oath in the same spirit; おめぇ is "you".
- **Ebisumaru**: Kansai dialect, cheerful and greedy for food, calls himself ワテ. In English: chatty,
  folksy, a little fussy ("y'know", "ain't"), never so thick that it is hard to read. ホニニッ, his cry
  of surprise, is "Honi-ni!".
- **Sasuke**: a clockwork ninja who ends his sentences with でゴザル. In English: formal and stiff, no
  contractions, often "sir" to Goemon.
- **Yae**: a kunoichi; lively, direct, plain speech.
- **The magistrate Kinemon**: pompous, old-fashioned, "ye" and "thou" only where he puts on airs.
- **The Marble Five** (from Goemon 2) end every sentence with っす: easy, mumbling "y'know".
- **The Mr. Goemon Gang** speak Nagoya dialect (だぎゃ, おみゃーら). In English: a rustic drawl, "y'all",
  "reckon", "we's", so that they never sound like Ebisumaru.
- **Kensuke** ends his sentences with ありんす, the speech of the old pleasure quarters. In English a coy
  "dearie".
- **Honorifics** are left out (ヤエちゃん is Yae, 金さん is Kin). Ebisumaru's 金はん is "ol' Kin".

## Glossary

One line a term: original, name chosen, source. "Official" means a Konami English release used it
(as listed in the English Wikipedia articles on the series' games); "pack" means the pack's own choice,
where no official English exists.

| Original | English | Source |
| --- | --- | --- |
| ゴエモン | Goemon | official (Mystical Ninja Starring Goemon, N64) |
| エビス丸 | Ebisumaru | official (N64) |
| サスケ | Sasuke | official (N64) |
| ヤエ | Yae | official (N64) |
| おみつ, おみっちゃん | Omitsu | official (N64) |
| 物知りじいさん | the Wise Man | official (N64) |
| ゴエモンインパクト | Impact | official (N64: the giant robot) |
| 両, 小判 | ryo | official (N64) |
| 大江戸, 江戸 | Edo; Great Edo where 大江戸 is a flourish | official (Goemon's Great Adventure: Edo) |
| マッギネス | McGuinness | pack (Goemon 2 was Japan-only; English Wikipedia's spelling) |
| マーブルレッド, ブルー, グリーン, ブラック | Marble Red, Blue, Green, Black | pack |
| Ｍｒ五右衛門 | Mr. Goemon | pack (the impostor, written in the kanji of the historical Goemon) |
| Ｍｒ五右衛門団 | the Mr. Goemon Gang | pack |
| 遠山金衛門, 金衛門 | Magistrate Kinemon Toyama, Kinemon | pack (a parody of the magistrate Toyama Kinshiro) |
| ペルリ, 天狗ペルリ | Peruri, Tengu Peruri | pack (the period Japanese name of Commodore Perry) |
| 天狗 | tengu | pack (the mountain goblin, as English reference works write it) |
| 天狗教 | the Tengu cult | pack |
| 鈴 | Suzu | pack |
| ほろほろ寺 | Horohoro Temple | pack |
| はぐれ町 | Hagure Town | pack |
| 奉行, 奉行所 | the magistrate, the magistrate's court | pack |
| 瓦版 | broadsheet | pack |
| 手配書 | wanted poster | pack |
| 御用だ | "In the name of the law!" | pack |
| キセル | pipe | pack (Goemon's weapon, a kiseru) |
| 三種の神器 | the Three Sacred Treasures | pack (the Imperial Regalia; English reference works) |
| 神器 | sacred treasure | pack |
| 草薙剣, 神器の刀 | the Kusanagi Sword | pack |
| 八咫鏡, 鏡 | the Yata Mirror | pack |
| 八尺瓊勾玉, 勾玉 | the Yasakani Jewel | pack |
| 天岩戸 | the Heavenly Rock Cave | pack |
| 八岐大蛇 | Yamata no Orochi | pack (English reference works) |
| 七福神 | the Seven Lucky Gods | pack (English reference works) |
| 恵比寿神 | Ebisu | pack |
| 七福玉 | Lucky Orb | pack |
| 宝船 | the Treasure Ship | pack |
| ひょっとこ, 火男 | Hyottoko | pack (the mask) |
| 甘党地獄 | Sweet Tooth Hell | pack |
| 旅日記 | Travel Diary | pack (a save file) |
| 里 | ri | pack |
| 天狗面 | Tengu Mask | pack |
| 御札 | Talisman (an item); charm | pack |
| 妖怪 | yokai | pack |
| 和尚 | the head priest | pack |
| 宝物殿 | the treasure hall | pack |
| 徳太郎 | Tokutaro | pack |
| ケン助 | Kensuke | pack |
| スーパー小判 | Super Coin | pack (小判 is the coin Goemon throws here, not money) |
| パワーグローブ | Power Glove | pack |
| 下町奉行 | the Downtown Magistrate | pack |
| 桜吹雪 | the cherry blossom tattoo | pack (the tattoo of the magistrate Kinemon parodies) |
| Ｌボタン, 十字ボタン | the L Button, the +Control Pad | Nintendo's English manuals |

## What has been done

- `system`: all but `system.02876`, which looks like the characters drawn for the sound test's labels and
  is left as the game has it.
- `stage_demo`: all of the storyteller.
- Area 1: the scenes `demo_a1_n0` to `demo_a1_n11`, the town `npc_town1_n0` to `npc_town1_n4`, its shops
  `shop_area1`.

## What has been seen on screen

Builds were run from power-on in DeSmuME (ventris's `ds-probe`):

- The save screen's prompt (`system.03056`).
- The whole opening, `stage_demo.12722` to `stage_demo.21132`, written across, to the chapter title card.
- Not yet: the trial scene and the rest of area 1 with this pack's own text (the trial was seen with test
  text, which showed the box's width and its pages), the shops and the town.
