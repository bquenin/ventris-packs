# G.O.D pure in English: notes

Working notes for the pack: how the strings are written, the names and terms chosen, and what is still
open. The pack is a first full pass: every area's dialogue, the menus, the lists, the shops, the notebook
and the diary. The party's names and the main ones below are agreed with the owner.

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

## People met later

| Japanese | English | note |
| --- | --- | --- |
| ミャア市長, ミャア姫 | Mayor Myaa, Princess Myaa | Myaa Town |
| ダン・キチ | Dan Kichi | written in full in dialogue; `Kichi` as a party name |
| Ｄｒ．Ｚ | Dr. Z | Inuyama Zoo |
| ダークソルジャー | Dark Soldier | |
| グラバー, ネモ船長 | Glover, Captain Nemo | Nemo ends lines with `ahoy` |
| エリカ | Erika | Mirage House |
| ギボばあ | Granny Gibo | |
| ケン, クラーク | Ken, Clark | Snow Village; Clark quotes "be ambitious" |
| ルカ | Luka | the dolphin; his いるか tic is `fin`, with a pun on porpoise |
| ミハエル | Michael | |
| Ｍｒ・チャン | Mr. Chan | |
| ウォン長官, シュウ大人 | Director Wong, Master Shu | Honmaka Town |
| シロワゼット博士, アカワゼット博士 | Dr. Whitoiset, Dr. Redoiset | Croiset's twin and cousin |
| ビシュヌール | Vishnur | Angkor Wat |
| トン, チン, カン | Ton, Chin, Kan | the monk's disciples |
| ワレンコフ, ワーニャ | Warenkov, Vanya | |
| カクレンボじいさん, タルコフスキー | the Hide-and-Seek Geezer, Tarkovsky | |
| ロシア大統領, 助役 | the Russian President, the Deputy | |
| ゾルバ, イワン | Zorba, Ivan | |
| チャーチル長官, ピエール長官 | Director Churchill, Director Pierre | |
| エリザ | Eliza | |
| クリューエル将軍 | General Crewel | |

## Ways of speaking

- Myaa Town folk end lines with `myaa` (Nagoya's みゃあ), sometimes `dagya`, `zura`, `nyaa`.
- Vladivostok and the Trans-Siberian staff say `vich` (だびっち).
- Chinese-accented speakers (アル, ある) say `-aru`.
- Free Paris says `darling` (ざんす); Free London speaks plainly (だす is dropped).
- Kansai speakers (Dengana, the info dealer) speak like a street hustler: `ya`, `whaddaya`.
- Osore Village (Tohoku) speaks rural: `ain't`, `I tell ya`.

## Areas written short

Area 131 (Honmaka Town) and 157 (the UN Building) were written tersely when the heap left them little room;
with the door patch and letter pairs every area now has tens of KB to spare, so they could be loosened.

## Abbreviations

- Item names have about 72 pixels, ten narrow letters: `Big Pow.Wtr`, `Titan Swd`, `CossackCap`, `Fire Chain`
  (necklaces), `Zori` (sandals), `Ess.` (essence), `Wtr` (water). Dialogue that names an item in its own text
  writes it in full.
- The seven chakras have one cell each: K (気, ki), W (知, wisdom), H (癒, healing), S (霊, spirit), N (陽, sun or
  nature), J (楽, joy), P (力, power). Chakra pairs are written `K×W`.
- Menu labels that the screen allows only 3 or 4 letters: `CHRG`, `CMD`, `SAV`, `LOD`, `AUT`, `MIS`, `ZZZ`, `DAZE`.

## Left in Japanese

- Area 178, the developers' debug room, and the placeholder lines such as `エアーズロックのＮＰＣ１です`.
- The phone keypads (digits and marks), which are not words.
- The battle scripts' text (battle.txt) is not changed.

## Open

- コウラン's name (written Kouran).
- The names marked **reading**, against the SNES patch when its spelling can be found.
- Name entry is out of scope; the party's default names are set in program.txt.

## Built

The whole pack builds with nothing refused (ventris main 0e8d3d7): 8,794 dialogue strings in 91 areas, 3,297
program strings taking 43,073 of the room's 70,379 bytes, 61 menu labels; 85 characters and 155 pairs in the
renderer; 105,220 bytes of the heap free at the tightest moment.

## Seen on screen

All from power-on in PCSX-Redux. Screens past the opening were reached by setting the game's mode in memory,
not by playing to them.

- The opening at home (096): narrow, even letters, lines wrapped in the window.
- Under Neo-Kobe (105) after the 107 to 105 door, and the casino of Kowloon Tower (179) after the 131 to 179 door.
- The caption that names Tsukubane Village on a first visit, whole and centred.
- A shop: its title centred, its labels (`BUY`, `SEL`, `LEAVE`), the clerk's greeting, the item list and prices.
- A battle: monster names with their letters, the command labels, the Tactics lines, damage messages.
- The equipment screen, the camp diary with its Overwrite? Yes/No, the notebook (Croiset Notes).
- Not seen: the Chakra, Psycho and Skills screens, story dialogue past the first areas, the ending, field
  "Got" messages and battle drops, and real hardware.
