# G.O.D pure in English: notes

Working notes for the pack: how the strings are written, the names and terms chosen, and what is still
open. The pack is in progress; the party's names and the main ones below are agreed with the owner.

## How it is made

Machine translated from the game's own Japanese script, directed by bquenin, and not reviewed by a person
who reads Japanese.

G.O.D pure is the PlayStation remake of G.O.D: Mezameyo to Yobu Koe ga Kikoete (Super Famicom, 1996).
Neither was released in English, so no name is official. The names follow the English fan translation of
the Super Famicom game by Dynamic-Designs (2018) where it is known, so that a player of one finds the same
names in the other; the owner of this pack chose to. Only names are taken from it: every line is
translated from the PlayStation game's own Japanese.

Sources, in the tables below:

- **SNES patch**: the Dynamic-Designs translation, as its patch file and the TV Tropes page on it give the
  name.
- **real**: a real person, place or work, written as English writes it.
- **reading**: the plain reading of the katakana; the SNES patch's spelling is not known yet.
- **pack**: this pack's own choice.

## How the strings are written

- American spelling.
- A line of dialogue is written unbroken. The build breaks it to fit the window, so a line break in a
  string is there on purpose: a list, a choice, a sign.
- Each character keeps their voice. Rough stays rough, polite stays polite.
- Japanese quotation brackets become straight double quotes; 《》 stay as they are.
- Wide Latin letters and digits become plain ones (`LEVEL 10`, `HAPPY 9`).
- A name of the party is in the line as its tag (`{NAME:19}`), never written out, because the player
  names the party.

## Party

The names are the strings `program.701264` to `program.701294`. A new game gives them, and the player
renames each member when they join. A name is at most 6 cells, one character to a cell; the slot is the game's, and is not made longer. Names are written in capitals, since the menus draw them in a font without lowercase letters, and so are the nicknames for Gen's mother the player picks from (`096.075` to `096.087`). The pack does not give the names yet: the program's strings share the room they had, and the English names need 6 bytes more than the Japanese ones; they go in with the program's text, which frees room.

| string | Japanese | English | source |
| --- | --- | --- | --- |
| 701264 | ゲン | Gen | SNES patch |
| 701268 | ヒース | Heath | SNES patch |
| 701272 | ミナ | Mina | SNES patch |
| 701275 | アイ | Ai | SNES patch |
| 701278 | バジル | Basil | SNES patch |
| 701284 | レム | Lem | SNES patch |
| 701287 | ダン・キチ | Kichi | pack: `Dan Kichi` is 9 cells; dialogue writes him in full |
| 701294 | ママ (Gen's mother, renamed by the player) | Mama | SNES patch |

## People

| Japanese | English | source | note |
| --- | --- | --- | --- |
| ミハエル | Michael | SNES patch | Gen's half-brother |
| クリューエル | Crewel | SNES patch | General Crewel |
| ラ・ムー | Ra Mu | SNES patch | the aliens' leader |
| ルシファー | Lucifer | SNES patch | |
| カタストロフ | the Great Catastrophe | SNES patch | 偉大なるカタストロフ様 |
| ファラ | Fahrah | SNES patch | |
| ギボ | Gibo | SNES patch | Ai's grandmother |
| オババ | Granny | pack | how Ai speaks of Gibo |
| バット | Batty | SNES patch | the bat |
| オバケコウモリ | Ghost Bat | pack | Batty, before he is named; he calls himself ボクちん, `widdle me` |
| ガキ大将 | Brat Boss | pack | the Tsukubane gang leader; his gang call him おやびん, `the Boss` |
| ムサシ | Musashi | real | what the Brat Boss calls Gen, playing at samurai rivals |
| クローゼット博士 | Dr. Closet | reading | Croiset's daughter; the name puns on his |
| 隊長 | Captain | pack | of the Attack Team |
| ポセイドン | Poseidon | real | King of Atlantis |
| リンダ | Linda | SNES patch | |
| サム | Sam | SNES patch | the UN worker |
| チャーチル | Churchill | SNES patch | chief of Bless in London |
| レノン | Lennon | SNES patch | chief of Bless in New York |
| マッカートニー | McCartney | SNES patch | his deputy |
| ワシントン | Washington | SNES patch | M.K. Washington, president |
| グラバー | Glover | SNES patch | of Nagasaki |
| クロワゼット博士 | Dr. Croiset | SNES patch | |
| オレンジワゼット, アカワゼット, シロワゼット, ミドリワゼット | Dr. Orangeoiset, Dr. Redoiset, Dr. Whitoiset, Dr. Greenoiset | pack | colour puns on クロ (black) in Croiset, kept as puns; each string says so in a `# ` comment |
| ジムジィ | Jimsy | SNES patch | |
| アカシ長官 | Director Akashi | reading | |
| コウラン | open | | a Chinese beauty; the reading is Kōran |
| ゾルバ | Zorba | reading | |
| ワレンコフ | Warenkov | reading | |
| ワーニャ | Vanya | reading | a great thief |
| イワン | Ivan | reading | |
| ピエール | Pierre | reading | |
| マッコイ | McCoy | reading | |
| クラーク | Clark | reading | |
| エリカ | Erika | reading | |
| アリス | Alice | reading | owner of the theme park |
| キティ | Kitty | reading | |
| タラン参謀 | Staff Officer Taran | reading | of Amazon Bless |
| 大神官キァタ | High Priest Kiata | reading | |
| シャハラ姫 | Princess Shahara | reading | |
| 女王ラルワ | Queen Larwa | reading | |
| ツタンカーメン, ツタン | Tutankhamen, Tut | real | |

## Places

| Japanese | English | source |
| --- | --- | --- |
| ニホン | Japan | real |
| ネオコウベ | Neo-Kobe | SNES patch |
| ミャアタウン | Myaa Town | SNES patch |
| ホンマカタウン | Honmaka Town | SNES patch |
| ナガサキタウン | Nagasaki Town | SNES patch |
| イズモ | Izumo | SNES patch |
| ツクバネ村, ツクバネ山 | Tsukubane Village, Mt. Tsukubane | SNES patch |
| イヌヤマズゥ | Inuyama Zoo | SNES patch |
| リュウキュウ | Ryukyu | SNES patch |
| キュウシュウ | Kyushu | real |
| レムール村 | Lemur Village | SNES patch |
| カスバ村 | Kasbah Village | reading |
| シンキロウハウス | Mirage House | pack |
| キボウホテル | Hope Hotel | pack |
| 救いの家 | House of Salvation | SNES patch |
| 民宿ツクバネ屋 | Tsukubane Guesthouse | pack |
| ふるさと小学校 | Furusato Elementary School | reading |
| ブレスツクバネ支部, ツクバネブレス | Bless Tsukubane Branch, Tsukubane Bless | SNES patch, pack |
| ルナシティー | Luna City | SNES patch |
| ムー, アトランティス, レムリア, アララト | Mu, Atlantis, Lemuria, Ararat | SNES patch |
| チチェンイツア, ストーンヘンジ, アンコールワット, ナスカ, モアイ, エアーズロック | Chichen Itza, Stonehenge, Angkor Wat, Nazca, Moai, Ayers Rock | real |
| ウラジオ | Vladivostok | real |

## Groups

| Japanese | English | source |
| --- | --- | --- |
| ブレス | Bless | SNES patch |
| ネオコウベブレス, アマゾンブレス | Neo-Kobe Bless, Amazon Bless | SNES patch |
| アタックチーム | Attack Team | reading |
| ファティマリア | Fatimaria | SNES patch |
| エイリアン | aliens | SNES patch |

## Terms

| Japanese | English | source | note |
| --- | --- | --- | --- |
| 神の石 | God Stone | SNES patch | |
| コスモストーン | Cosmo Stone | SNES patch | |
| チャクラ | Chakra | SNES patch | |
| チャクラレベル, チャクラコマンド | Chakra Level, Chakra Command | SNES patch | |
| サイコ | Psycho | SNES patch | the psychic powers' command |
| まんじゅう | bun | SNES patch | |
| まんじゅう王 | the Bun King | SNES patch | |
| ハッピー９ | Happy 9 | reading | a card game |
| モンスター | monster | | |
| 日記 | diary | pack | the save: `Write in diary`, `Read diary` |
| クロワゼットノート | Croiset Notes | pack | the help notebook |
| ご本尊 | sacred relic | pack | the God Stone kept at Tsukubane Shrine |
| 不思議な力, 未知の力 | strange power, unknown power | pack | |
| ガマの油 | toad oil | real | |
| 〜まんじゅう, 〜まん | `... Bun`: Toad Bun, Corner Store Bun | SNES patch | each bun's name ends in Bun |
| 落ちこぼれ | washout | pack | what the Attack Team call Gen |
| 体力 | HP | pack | in `HP was restored` |

## Open

- While little of the game is translated, few kanji cells are free for pairs of letters, and pairs without a cell are drawn as full-width letters. Area 096 alone needs 484 pairs and has 278 cells. A full translation frees most of the 1,516 kanji; the English packs of games this size need about 1,200 to 1,700 pairs.
- コウラン's name.
- The names marked **reading**, against the SNES patch when its spelling can be found.

## Built

Areas 096 to 099 and 101 to 104 build with nothing refused.

## Seen on screen

- `096.109` to `096.112`, the opening at home, from power-on (PCSX-Redux). Pairs that found no cell show as full-width letters while few areas are translated; see Open.
