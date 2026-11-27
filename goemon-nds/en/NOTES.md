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
- **Numbers the game prints**: some strings are halves of a sentence around a number the game draws
  itself (a price, a count). A string that comes before the number ends with a space
  (`For this, it's `), and the one after it starts with one (` ryo, thank you.`). The build keeps
  those spaces.
- **Placeholders** the developers left in the script (`ちょうにん０`, `あるき７`, `うらない２`,
  `かりゅう、こども`, `やまたい６`, blank strings) are labels the player never sees, and are left as
  they are.
- **No boxes of our own**: `{0D}{0A}` is never added where the Japanese has none; its `/` (a line
  break) is dropped, since the build breaks lines itself.
- **Shops** (`shop_area*`) are written by a small script of the author's from a table of item names
  and the shopkeepers' lines, since every shop repeats the same strings.
- **The guide bubbles** (`gim_help_*`) keep the blank lines the Japanese has inside a string, as
  paragraph gaps; their single line breaks are dropped like any other.
- **Generated files**: `dojo` (four training halls with the same lines) and the `gim_help_*` files
  were written from small tables by a script of the author's, like the shops.
- **Quizzes**: the Tokaido quiz's fixed lines (`Oh? Are you a quiz contestant?`, `Correct!!`, `Too bad!!
  Wrong answer!!`, `Got 50 ryo in prize money!`) are word for word the same in every town.
- **Choices** (Yes/No, the quiz's answers, the shops' options) are drawn where the script puts them, at a
  fixed point (x 64 to 160), and are not wrapped; the box ends at x 208. A choice of n letters from x
  must end there: x + 8n <= 208. Checked from the scripts for every choice; only the last quiz's
  answers needed shortening, to "Basho" and "Hiroshige".
- **Windows**: only the scenes set a window of their own (the two dialogue boxes beside a face, 160
  dots wide); the towns, shops and guide bubbles use the default box, the same width.
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
  - **A spread holds at most 111 letters.** The two pages shown together (from one page turn,
    instruction 0x0A, or the start of a scene, to the next) draw each letter as a sprite; spaces and
    line breaks cost nothing. Past 111 letters the rest of the text is simply not drawn: the last
    page once stopped at "on their jo". Every spread is kept to 104 letters or fewer, which is why
    the chapter recaps are terse and the refrain is "Well, well! What fate awaits Goemon and his
    friends?". A small script of the author's counts them from the script's instructions.

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
- **Mr. Goemon's henchmen** (area 4, without their boss) call Goemon 親分 and talk like London
  toughs: "guv'nor", "see".
- **Tengu Peruri** speaks in katakana, a foreigner's careful Japanese. In English: stiff and formal, no
  contractions, polite even when gloating. Where he slips into Kansai for a line (アレヘンヤン), the
  English slips too, into a contraction and "y'know".
- **The Hyottoko brothers** end their sentences with っス: a "y'know" on almost every sentence.
- **Hitoe** ends with でござる like Sasuke but softer: "so it is".
- **The village master's wife** (the camp innkeeper) calls everyone "darling".
- **The Kagoshima porters**: "aye", "ye".
- **The yamamba** speaks Kumamoto dialect (なっせ) and laughs しぇっ、しぇっ: "dearie", "Sheh, sheh."
- **Masakado's ghost** speaks in katakana broken by commas: one word at a time, "I, am, Masakado...".
- **Amaterasu** calls herself ワラワ: regal and old-fashioned, no contractions; laughs "Oh-ho-ho-ho!".
- **Susanoo** is a crying child who calls Amaterasu おねいちゃん: "Sis", "Sniff...".
- **Children who lisp** (area 4's kidnapped boy): "fank you", "wiv", "scawy", lightly. Those who end
  with でちゅ (Fujikawa's guide, Kyo's kimono seller) lisp on s: "Thith is the town of Fujikawa".
- **The Seven Lucky Gods**: Ebisu a grumpy old geezer; Benzaiten ends with でおじゃる, a court lady's
  speech: "I declare"; Jurojin and Bishamonten plain and dignified; Hotei draws out his vowels
  (でぇす): "Who iiis it?"; Fukurokuju is a show-off who types emoticons, and the emoticons stay as the
  game has them, with English words for their Japanese ones (`v(ー_ー)Tsk tsk`, `(lol)` for （笑）).
- **The Otafuku sister** ends with ありんす like Kensuke: "dearie".
- **Kinemon unmasked** (from area 7) drops his "thou" and talks rough: "I'm gonna rule this country".
- **Plasma** ends every sentence with ぷらずま: "..., plasma." His laugh ぷぷぷぷ is "Pupupupu...".
- **Kurobee** (the cat) ends with ニャ: "nya".
- **McGuinness**, like Peruri, speaks katakana: formal, no contractions, cheerful.
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
| 天狗様 | Lord Tengu | pack |
| 天狗岩 | Tengu Rock | pack |
| 信者のツボ | Believer's Pot | pack |
| 今右衛門 | Imaemon | pack |
| インパクトコントローラー | Impact Controller | pack |
| サスケ風船 | Sasuke Balloon | pack |
| 花火爆弾 | firework bombs | pack |
| 通行手形 | Travel Pass | pack |
| 緑の巾着, 黄色の巾着, 青の巾着, 赤の巾着 | Green Purse (300 ryo), Yellow Purse (500), Blue Purse (700), Red Purse (999) | pack |
| 弁財天, 寿老人, 毘沙門天 (昆沙門天 in the script), 布袋尊, 福禄寿, 大黒天 | Benzaiten, Jurojin, Bishamonten, Hotei, Fukurokuju, Daikokuten | pack (English reference works) |
| オナラの術 | the Fart Technique | pack |
| 反射手裏剣 | the Reflecting Shuriken | pack |
| 大天狗 | the Great Tengu | pack (Peruri's giant weapon) |
| 桜さん | Mr. Sakura | pack (Peruri's name for Kinemon, after his tattoo) |
| おたふく三姉妹, 大福 | the three Otafuku sisters, Daifuku | pack |
| 福笑 | fukuwarai | pack |
| ノストラ | Nostra | pack (the hidden collectibles) |
| 怒り, 乱れ, 戦国, 天女の修行道場 | the training hall of Wrath, Chaos, the Warring States, the Celestial Maiden | pack |
| 大ダコの術, 乱れサイコロの術, 戦国インパクトの術, 天女の術 | the Giant Octopus Art, the Chaos Dice Art, the Warring States Impact Art, the Celestial Maiden Art | pack |
| 大岡越前守, 根岸肥前守 | Ooka, Lord of Echizen; Negishi, Lord of Hizen | pack (historical magistrates) |
| ゆき姫 | Princess Yuki | pack |
| クロべえ, 小判ネコ親分 | Kurobee, Boss Koban Cat | pack |
| 千秋楽 | Senshuraku | pack (McGuinness's giant robot in Goemon 2) |
| 藤川, 御油, 赤坂, 坂下, 水口, 大津, 三条大橋 | Fujikawa, Goyu, Akasaka, Sakanoshita, Minakuchi, Otsu, Sanjo Bridge | the stations' names |
| バレリーナドリル | Ballerina Drill | pack |
| ホーミングバズーカ | Homing Bazooka | pack |
| 一重, ひとえ | Hitoe | pack |
| ひょっとこ兄弟, ひょっとこ踊り | the Hyottoko brothers, the Hyottoko Dance | pack |
| ヤグラ | the tower | pack |
| ヤマンバ | yamamba | pack (the mountain hag, as English reference works write it) |
| マサカド | Masakado | pack (Taira no Masakado; his ghost) |
| アマテラス, スサノオ | Amaterasu, Susanoo | pack (English reference works) |
| ちょうちん魔人 | the Lantern Demon | pack |
| プラズマ | Plasma | pack (the fortune teller) |
| エドレンジャイ, ニンジャイ | the Edo Rangers, the Ninja Rangers | pack |
| 東海道五十三次ウルトメクイズ | the Tokaido Fifty-Three Stations Ultro Quiz | pack (a parody of the TV quiz show ウルトラクイズ) |
| 竜宮城 | the Dragon Palace | pack |
| 江尻, 府中, 舞阪, 二川, 見附, 新居, 袋井, 白須賀 | Ejiri, Fuchu, Maisaka, Futagawa, Mitsuke, Arai, Fukuroi, Shirasuka | the stations' names |
| Ｌボタン, 十字ボタン | the L Button, the +Control Pad | Nintendo's English manuals |

## What has been done

- `system`: all but `system.02876`, which looks like the characters drawn for the sound test's labels and
  is left as the game has it.
- `stage_demo`: all of the storyteller.
- Everything else: every scene (`demo_a1_*` to `demo_a8_*`, `demo_ending`, `demo_goe12`), every town
  and inn (`npc_town1_*` to `npc_town7_*`), the shops, the training halls (`dojo`), the porters
  (`kagoya`), Plasma (`purazuma`), the guide bubbles (`gim_help_*`) and the other people (`npc_*`).
  The strings the pack leaves out are all placeholders (above) or `system.02876`.

## What has been seen on screen

Builds were run from power-on in DeSmuME (ventris's `ds-probe`):

- The save screen's prompt (`system.03056`).
- The whole opening, `stage_demo.12722` to `stage_demo.21132`, written across, to the chapter title card.
  Seen again after the spreads were shortened: the opening runs through 16654 to the title card, and
  the last spread (20914, 20994, 21132) is drawn whole and waits for the button. Pressing A while a
  page is still being written skips to the next page, so a check presses nothing on the page it reads.
- The start of the trial (`demo_a1_n0`): the magistrate's entrance and his first speeches, wrapped to
  the box, with a fourth line going on in a cleared box. The name plates beside the faces are pictures,
  and stay in Japanese.
- A guide bubble (`gim_help_pcmn_r00.380`, at the rope in the underground passage after the trial):
  drawn in the top screen's box, wrapped to it, each blank line starting a new box as in the Japanese.
- Area 1, played on from the trial: the underground passage and the soy sauce shop's cellar, with their
  guide bubbles (`gim_help_syouyuya.360`, `.756`, `.928`, `gim_help_p10400_o00`, `gim_help_p10502_o00`);
  Yae's scene in town (`demo_a1_n2`), Omitsu's (`demo_a1_n4`, every string), Suzu's (`demo_a1_n5`, every
  string) and the head priest's (`demo_a1_n6`, every string); Omitsu at the teahouse (`npc_cha1_n0.0822`),
  Tokutaro (`npc_town1_n0`), the boatmen with their Yes/No (`npc_town1_n1.2792`, `.2958`,
  `npc_horohoro1_n0.1072`, `.1232`); the save prompt, "Saved." and "Return to the title screen?". All
  fit their box, break at spaces and draw every letter. What they showed: the blinking prompt covered
  the last two cells of a third line of 19 or 20 letters (`demo_a1_n2.2368`, `demo_a1_n6.1842`); the
  adapter now keeps the third line of each box to 18 cells, and the trial was seen built that way.
- Not yet: Kannon Hall and everything after it, the town by day with its shops, the quiz and the
  townspeople (at night, after the trial, they are not out), the other areas, and Fukurokuju's
  emoticons, whose ASCII parts are drawn from Unifont.
