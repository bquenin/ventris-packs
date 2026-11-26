# Tales of Destiny 2 in English: notes

Working notes for the pack: how the strings are written, the names and terms chosen, and what is still
open. The pack is in progress; it starts at the opening of the game.

## How the strings are written

- American spelling (`armor`, `forever`, `Mom`, `Dad`).
- A line of dialogue is written unbroken. The build breaks it to fit the bubble, so a line break in a
  string is there on purpose: a sign, a list, a choice.
- A string that is only a party member's name (`{NAME:01 00 00 00}`), an empty string, and the
  programmer's words (`notice`, `select`, `menu`, `wait_map_scroll();` and the like) are left out, so the
  game keeps its own.
- Each choice of a list keeps the wide spaces (U+3000) the game puts around it, and the `{03:..}` tag
  in front when the game has one.
- Japanese quotation brackets become straight double quotes. Wide Latin letters and digits become
  plain ones (`SP`, `TP`, `NORMAL`).
- `♪` and `★` are kept where the game has them.
- A stock line is written the same way everywhere it appears (below).
- A skit line has a budget of letters. A skit runs on a clock set by its voices and cannot be paused,
  so a line has to finish typing before the game removes it. The pack asks the build for a faster typing
  pace in skits; the build never types faster than 5 frames a letter and refuses a line that still would
  not finish in time, so such a line is shortened here. Loni's `バ〜カ！` is `You du~mmy!` in every skit.

## Party

| tag | name |
| --- | --- |
| `{NAME:01 00 00 00}` | Kyle |
| `{NAME:02 00 00 00}` | Reala |
| `{NAME:03 00 00 00}` | Loni |
| `{NAME:04 00 00 00}` | Judas |
| `{NAME:05 00 00 00}` | Nanaly |
| `{NAME:06 00 00 00}` | Harold |

The names themselves are strings of the lists (`program.1063896` to `program.1064000`), and this pack
gives all six. A new game copies them into the save, and a player can rename a character on the Status
screen, to at most 12 columns. The build counts a name tag at the width of the name the pack gives, so
a line breaks as it will be drawn with these names.

## People

| Japanese | English | note |
| --- | --- | --- |
| スタン＝エルロン | Stahn Aileron | |
| ルーティ＝カトレット | Rutee Katrea | |
| リオン | Leon | |
| イレーヌ | Ilene | a signature on the Oberon papers |
| レンブラント | Rembrandt | a signature on the Oberon papers |
| フィリア＝フィリス | Philia Felice | of Straylize Temple |
| ウッドロウ＝ケルヴィン | Woodrow Kelvin | the Japanese name, not the one the first game's American release gave him |
| マリー | Mary | |
| ヒューゴ | Hugo | |
| エルレイン | Elraine | `Lady Elraine` for エルレイン様 |
| バルバトス | Barbatos | 06318.158 is this name spelled wrongly in the game; the pack writes it right |
| ガゼル | Gazelle | a townsman who is only spoken of |
| the orphans | Cinnamon, Basil, Uni, Rim, Blue, Salt, Jan, Mina, Tonia | |
| めくりのジョー | Joe the Flipper | |
| 雷光のネルソン | Nelson the Lightning | |
| つむじ風の{NAME} | Whirlwind {NAME} | |

Speakers without a name: `Woman` (おばさん), `Young Woman` (女性), `Girl` (女の子), `Old Man` (おじいさん),
`Old Woman` (おばあさん), `Man` (おじさん), `Young Man` (青年), `Boy` (子供), `Bucket Man`, `Rich Man` and
`Rich Lady` (both 富豪 in the game), `Librarian`, `Shiny-Loving Maid`, `Mystery Warrior`, `Veteran`,
`Rookie`, `Too Veteran`, `Son`, `Chef`, `Grocer`, `General Store`, `Outfitter`.

## Places

Cresta, Cresta Forest, Dunamis Orphanage, Laguna Ruins (ラグナ遺跡), Darilsheid, Aigrette, Aquaveil,
Heidelberg, Straylize Temple (ストレイライズ神殿).

Captions: `古都ダリルシェイド` is `Darilsheid, the Old Capital`; `ダリルシェイド地下水路` is
`Darilsheid Underground Waterway`.

## Terms

| Japanese | English |
| --- | --- |
| アタモニ神団 | the Order of Atamoni |
| アタモニ神 | Atamoni |
| 四英雄 | the Four Heroes |
| 神の眼 | the Eye of God |
| 神のたまご | God's Egg |
| オベロン社 | the Oberon Corporation |
| レンズ | Lens, Lenses |
| レンズハンター | Lens hunter |
| ソーディアン | Swordian |
| ディムロス | Dymlos (Stahn's Swordian) |
| ガルド | Gald |
| 称号 | title |
| スクリーンチャット | Screen Chat |
| イクシフォスラー | the Ixifosler |
| リファイン | Refine, to refine |
| スロット | Slot |
| エンチャント | Enchant |
| ユニークアイテム | Unique Item |
| 特技 | arte |
| 奥義 | arcane arte |
| 秘奥義 | mystic arte |
| 術, 晶術 | spell |
| 追加特技, 追加晶術 | follow-up arte, follow-up spell |
| 通常攻撃 | normal attack |
| スピリッツ, ＳＰ | Spirits, SP |
| スピリッツブラスター | Spirits Blaster |
| プレスガード | Press Guard |
| テクニカルスマッシュ | Technical Smash |
| フィールドオブエフェクト | Field of Effect (FOE) |
| バトルグレード | Battle Grade (`GRADE`) |
| 受身 | recovering |
| 作戦 | strategy |
| ステータス異常 | status ailment |

## Stock lines

Lines the game says in many places are worded the same everywhere:

- Have a safe journey.
- That will be … Gald. Will you stay the night?
- Will you stay the night?
- Please rest well.
- Good morning.
- You do not have enough money.
- We look forward to seeing you again.
- Obtained ….
- Found …, but you can carry no more.
- There is nothing here.
- Received ….
- … joined the party.
- It won't open.
- It is pitch dark. You cannot see a thing.
- ?????
- … earned the title "…".
- They seem to be talking about "…". Listen in?

## From Darilsheid to Heidelberg

Names and terms settled while writing scripts 06337 to 06435. Spellings of names from the first game
follow its English release where one is known, written from memory and worth checking; the rest are
readings of the sounds.

| Japanese | English |
| --- | --- |
| カルバレイス | Calvalese |
| フィッツガルド | Fitzgald |
| ファンダリア | Phandaria |
| セインガルド | Seinegald |
| ノイシュタット | Neustadt |
| スノーフリア | Snowfria |
| リーネ | Lienea |
| チェリク | Cherik |
| ホープタウン | Hope Town |
| カルビオラ | Calviola |
| ハーメンツヴァレー | Harmentz Valley |
| ジェノス, サイリル | Janos, Cyril |
| 白雲の尾根 | White Cloud Ridge |
| デビルズ・リーフ | Devil's Reef |
| ストレイライズ大神殿 | the Great Temple of Straylize |
| 大聖堂 | the cathedral |
| 天空都市ダイクロフト | the sky city Dycroft |
| 空中都市 | aerial city |
| ベルクラント | Belcrant |
| ラディスロウ | Radisrol |
| 飛行竜 | the Flying Dragon |
| 外殻 | the Outer Shell |
| 天地戦争 | the War of Heaven and Earth |
| 地上軍 | the Surface Army |
| 神の眼の騒乱, ヒューゴの乱 | the uprising over the Eye of God, Hugo's uprising |
| 聖女, 輝きの聖女 | the Saint, the Radiant Saint |
| フォルトゥナ | Fortuna |
| エルレインさま, フィリアさま | Lady Elraine, Lady Philia (`さん` is the bare name) |
| ウッドロウさま, 英雄王 | King Woodrow, the Hero King |
| バルバトス＝ゲーティア | Barbatos Goetia |
| リオン＝マグナス | Leon Magnus |
| ヒューゴ＝ジルクリスト | Hugo Gilchrist |
| グレバム＝バーンハルト | Greybum Bernhardt |
| イレーヌ＝レンブラント | Ilene Rembrandt |
| リリス | Lilith (Kyle calls her Aunt Lilith) |
| リムル | Rimul |
| マイティ＝コングマン | Mighty Kongman |
| チェルシー＝トーン | Chelsea Torn |
| ウィンターズ | Winters |
| 漆黒の翼: グリッド, ミリー, ジョン | the Dark Wings: Grid, Millie, John |
| フォルネウス, 海の主 | Forneus, the lord of the sea |
| アルジャーノン号 | the Algernon |
| サバディーチョ | Sabadicho |
| ベルセリア, ベルセリウム | Berselia (the flower), Berselium (the metal) |
| ソーサラーリング, ソーサラースコープ | Sorcerer's Ring, Sorcerer's Scope |
| グミ | Gel |
| ねこにん | Katz |
| 魔神剣 | Demon Fang |
| 称号の例: 疾風の…, 雷鳴の…, 黒衣の…, 陽光の…, 流星の…, ねぐせ… | Whirlwind …, Thunder …, Black-Clad …, Sunshine …, Shooting Star …, Bedhead … |

Speaker labels added: Knight, Young Lady (`お姉さん`), Priest (`司祭`), Pastor, Cleric (`神官`), Worshipper,
Visitor, Guard (`衛兵`), Sentry (`警備兵`), Guardsman, Soldier, Swordsman, Scholar, Merchant, Traveler,
Woodcutter, Sailor, Captain, Passenger, Ship's Doctor, Quartermaster, Ticket Seller, Ticket Office, Innkeeper,
Inn Reception, Shop Girl, Food Stall, Maid, Guide Maid, Part-Timer, Bartender, Head Chef, Waiter, Waitress,
Blacksmith, Weapon Shop, Armor Shop, Outerwear Shop, Accessory Shop, Announcer, Manager, Spectator, Thug,
Doctor, Judge, Townsperson, Wife, Husband, Mother, Village Head, Village Head's Daughter, Granny Maggie,
Uncle Bob, Cat-Loving Old Man, Peeping Hero, Card Man, Mach Boy, Middle-Aged Mach, Entry Girl, Lass,
Young Girl, Little Boy, Youth, Old Guy, Wealthy Man, Old Salmon Man, Brother, Collector, Salesman,
Patrol Officer.

Ways of speaking kept across scripts: John of the Dark Wings ends his sentences "he is", "I am"; the
snobbish lady says "don't you know"; the fortune-teller Sabadicho draws out his last word ("I a~m"); the
Katz says "mew"; Loni's `バ〜カ` is "You du~mmy".

More names, from scripts 06436 to 06499:

| Japanese | English |
| --- | --- |
| ヒートリバー | Heat River |
| ジャンクランド | Junkland |
| レアルタ | Realta |
| 天上人, 天上軍 | the Heaven Dwellers, the Heavenly Army |
| ソーディアン: ディムロス, アトワイト, クレメンテ, イクティノス, シャルティエ, ベルセリオス | the Swordians Dymlos, Atwight, Clemente, Igtenos, Chaltier, Berselius |
| シャル | Chal (Judas's name for Chaltier) |
| サブノック, ガープ | Sabnock, Gaap |
| ルー | Lou (Nanaly's brother) |
| マリー＝エージェント, ダリス | Mary Agent, Dalis |
| ジョニー＝シデン | Johnny Shiden |
| レギーナ, ジニー (バージニア), サーガ | Regina, Ginny (Virginia), Saga |
| ミーシャ, ラーク, ニャーニャ | Misha, Lark, Nyanya (a kitten) |
| ミヤ, ウォルト | Miya (the architect), Walt |
| ヘレン, トッシュー, ダリエ | Helen, Toshu, Darie |
| バイラス, カミーユ, クルトン, ドナ, ビリー | Byrus, Camille, Crouton, Donna, Billy |
| 聖誕祭 | the Nativity Festival |
| 出産式, 保育管理官 | birth ceremony, childcare officer |
| 勅命状 | royal writ |
| 英雄門, 記念公園, 旧市街, 新市街 | Hero Gate, Memorial Park, Old Town, New Town |
| カンバラーベア | Kanbara Bear |
| やきそばパン | fried-noodle roll |
| 解析君二号改 | Analyzer No. 2 Mark II |

The game leaves a few of its own placeholders in the text (`p(kyle)`, `p(reala)`, `(reala)`), and they are
kept as they are. People in the game take the scientist Harold for a man, so their lines say "he".

A helper script fills in lines the pack already has: the stock lines above, the cooks, the seller of
refining bottles, the piles of Lenses in the mine, and any string whose Japanese is word for word one
already translated. So the battle lessons first written for Cresta read the same in every town.

## From Hope Town to the end

| Japanese | English |
| --- | --- |
| 聖地カルビオラ | Calviola, the Holy Land |
| 蒼天都市ヴァンジェロ | Vangelo, the Azure City |
| 紅蓮都市スペランツァ | Speranza, the Crimson City |
| 黄昏都市レアルタ | Realta, the Twilight City |
| 命のレンズ | Lens of Life |
| フォルトゥナ神団 | the Order of Fortuna |
| 配給所, 回復施設, 資料室 | Distribution Point, Recovery Facility, Archive |
| 光のほこら | the Shrine of Light |
| ダンタリオン, サブノック, ガープ, グラシャラボラス | Dantalion, Sabnock, Gaap, Glasya-Labolas |
| 地上軍拠点, 物資保管所, 購買部 | Surface Army Base, Supply Depot, Commissary |
| ラディスロウ・作戦会議室 | the Radisrol: Operations Room |
| リトラー総司令, リトラー司令 | Commander-in-Chief Litler, Commander Litler |
| ディムロス＝ティンバー中将 | Lieutenant General Dymlos Timber |
| カーレル＝ベルセリオス | Karell Berselius (Lieutenant General, the strategist) |
| イクティノス少将, アトワイト大佐 | Major General Igtenos, Colonel Atwight |
| クレメンテ殿, クレメンテ老 | Master Clemente, old Clemente |
| ミクトラン, 天上王 | Miktran, King of Heaven |
| 工兵隊, ユンカース隊 | the Engineer Corps, the Junkers Corps |
| 突撃兵 | "the Stormer" |
| ベルクラント開発チーム, ラディッツ | the Belcrant development team, Raditz |
| ＨＲＸ−２型 | HRX-2 |
| スパイラルケイブ | the Spiral Cave |
| マスターキー, セルキー, バイオキー | Master Key, Cell Key, Bio Key |
| 十八年前のダイクロフト | Dycroft, Eighteen Years Ago |
| スタン＝エルロン, ルーティ | Stahn Aileron, Rutee |
| アクアヴェイル, モリュウ, 旅籠シデン, 領主館 | Aquaveil, Moryu, Shiden Inn, Lord's Manor |
| フェイト, リアーナ, エミリ, クレア | Fayte, Leanna, Emily, Claire |
| アクアラビリンス, マグナディウエス | the Aqua Labyrinth, Magnadeus |
| 自由を愛する男, 自由称号 | The Man Who Loves Freedom, free title |
| 町大工のゲンさん | Gen the Town Carpenter |
| カタコンベ: 罪, 闇, 死, 罰の祭壇 | the Catacombs: Altars of Sin, Darkness, Death, Punishment |
| 転生の門, 生誕への階段 | Gate of Rebirth, Stairway to Birth |
| 神のたまご: 上層部, 中層部, 下層部 | the Egg of God: Upper, Middle, Lower Level |
| デリスエンブレム | Derris Emblem |
| 地上軍拠点跡地 | Ruins of the Surface Army Base |
| チェルシーの小屋, ジェノス | Chelsea's Hut, Janos |
| ねこにんの村, のこ, おじじ, こねこにん | Katz Village, Noko, Grandpa, Katz Kitten |
| 空中都市の残骸 | Wreck of the Aerial City |
| スクリーンチャット | skit |
| 蒼破刃, 蒼破追蓮 | Azure Edge, Azure Lotus |
| 具現結晶 | Embody Crystal |

- In the altered world people carry numbers for names (RE-54609, SP-3116); they are kept as written.
- Harold calls Karell "my brother", and "brother" to his face; the last scene has her say it in full.
- Barbatos is "that ape" to Harold. Chaltier calls Judas "young master".
- The Katz end their lines with "mew". The kitten the party names says "myu", and "mya" once it lives
  with Grandpa; Judas remarks that the dialect is different.
- The shopkeepers of Aquaveil speak the dialect of Kyoto; here they speak a polite, old-fashioned English.
- The Man Who Loves Freedom drops English words in capitals into his speech (BYE, SOUL, ROUTE); they stay
  in capitals.
- The ladies of the Radisrol say "don't you know", as the snobbish lady of Aigrette does, and their
  breathless speeches have no stops, as in the game.

## The menus and the battle program

- Files 06798 to 06816 are the menu screens. The wording is built from one table of phrases, so a button
  reads the same on every screen: OK, Back, Details, Edit, Remove, Use, Discard, Cancel, Character.
- A label is kept to 7 letters where the game's own takes up to 6 bytes, and to 15 where it takes up to
  14, so that it fits the place the game gives it. That is why the item tabs read Access. (装身具), Key
  (貴重品), Food (食材), Charm (装飾品), Mail (鎧) and 2-Hand (両手), and the stats Aim (命中) and Mind (知性).
- "{name} & co. / earned "{title}"." is the menu's form of the notice the dialogue gives in full.
- File 08055 is the battle program: its strings cannot move, so each is cut to its own space. The lessons
  shown when a kind of arte is first learned are headed <Artes>, <Healing Spell>, <Attack Spell>,
  <Enchant>, <Arcane Arte>, <Follow-up Arte> and <Mystic Arte>, and a lesson is stored a line to a
  string, last line first. The resistances read Dark-R, Light-R and so on for want of room.
- Files 08178 onward name the enemies of each battle. The names are English readings of the game's own;
  those from myth and books take their usual spelling (Jabberwock, Nachzehrer, Hraesvelg, Nyarlathotep).
- In 08996 the map's place names are cut to their space: Shell (外殻), Western, Southern and Northern
  Mine, "Field: Around the Army Base".

## The skits

- Files 00056 to 01298 are the skits: 608 of them, 2,411 lines. A skit's line has a fixed time on screen,
  so each line is written to the number of letters the build allows it (the option `skit-pace` types a
  long line faster, down to the fastest pace the game has). A line is therefore often shorter than a
  full rendering of the Japanese would be; what is cut is filler, never the point of the line.
- Two lines stay as the game has them: 00054.001 (nothing in the script refers to it, so it cannot
  change length) and 00856.012 (its time allows no letters at all).
- The running jokes keep one name each: Loni is "Turned-Down Man" (ふられマン), Judas the "Masked Stalker",
  Nanaly the "Submission Artist", Harold "Little Baby-Face".

## The lists (program.txt)

- `program.txt` holds every list the menus read: artes, tactics, enchants, slot powers, equipment, items,
  food, recipes, titles, shop names, place names and the titles of the skits. All 3,249 strings that
  hold Japanese are translated.
- An arte has three strings: what it does, its reading and its name. The name is English ("Azure Edge")
  and the reading is the Japanese in Roman letters ("Sohajin"), so the line above a description reads
  "Azure Edge (Sohajin)". A skill's name is kept to 17 letters, the width of the Artes grid. Spell names
  are whole English names and many are wider than the 9 large letters the grid gives a spell.
- The room measured on screen sets the lengths: 44 letters on each of 2 lines for an arte, 39 a line for
  equipment and items (3 lines for an item), 42 on each of 3 lines for a title, 22 letters for the name
  of a piece of equipment, 25 for an item, 28 for a title. Skit titles are kept to 30.
- 昇華晶術 is a "sublime spell". 熟練度 is "aptitude", グミ a "gel", 図鑑 a "book" (Monster Book,
  Collector's Book). The weapons and armor named 「グリム…」 share one line: "…with a power out of
  legend, named for brothers who wrote old tales."
- Names out of myth and history take their usual spelling: Laevateinn, Ama no Murakumo, Arondight,
  Caladbolg, Gae Bolg, Megingjord, Hauteclaire. The seeds (Charac, Oriola, Penpen, Dolgenia, Ranakeal,
  Estema, Pompom) and a few others (Waiapolo, Itatoma) are readings of the sounds.
- A shop is written "Kind: Name" (Weapons: Braveheart, Food: Fresh Market, Supply Unit: Rob Roy). The
  shops of Katz Village are translated, since their names are cat jokes: Grooming, Claw Sharpener,
  Bonito Flakes, Paw Pads, Catnip.
- Two jokes are turned round to work in English: the carrot is called "ninjin" "in an eastern tongue"
  where the game says "carrot" "in a foreign tongue", and the title 迷探偵 is "Defective Detective".
  The card game 神経衰弱 is "Concentration", so its title jokes about wearing out the nerves.
- A handful of strings cannot move and were cut to their own space: 332, 918 ("No name"), 1282, 1446,
  1572 and the skit title 2816 ("On My Mind").

## The quiz books and minigames

- Files 06167 and 06178 to 06299 are the quiz books and the small picture, sound and counting games:
  90 scripts, 5,229 strings changed. Six of them (06184 to 06189) are the question banks on Tales of
  Phantasia, on this game and its prequel, on Tales of Destiny, on Tales of Eternia, on the series'
  books, discs and side games, and on this game again.
- A string in these files cannot move, so each is written to the bytes the game's own takes: a kana or
  kanji is two bytes and a Latin letter one. That is why answers are terse ("No. 2", "Time's up",
  "Wht", "Lt.G") and why a few names are shorter here than in the lists: "Good Bro" for the title Good
  Big Brother, "Mars" for War God, "GodEye" for the Eye of God, "Laguna" for the Laguna Ruins, "Storm"
  for the Stormer, "Ranz" and "Hanz" for Ranzo and Hanzo.
- Where an answer is a single kanji (two bytes), the choice stays as the game has it and the question
  says what it means: "(剣 sword, 盾 shield)", "(蛇 = snake)", "(海竜 = sea dragon)", "(犬 dog, 亀
  turtle)", "(白 white, 赤 red)".
- Names from the other games are the usual romanised ones, from memory: Cress Albane, Chester
  Barklight, Mint Adnade, Claus F. Lester, Arche Klein, Suzu, Dhaos; Reid, Farah, Keele, Meredy, Ras,
  Craymel, Aurora Artes, Mintche, Rasheans. 晶霊 is "Craymel" in the Eternia questions.
- Left as the game has them: the placeholder strings that begin with `**`, the template question
  ("「せいかい」を選べ" and its answers) at the head of each bank, and, in the fill-in quizzes 06190 to
  06195, the pattern with the blanks and the answer (雷光の○○○○ / 雷光のネルソン). In those six the
  question and the replies are English.
- Jokes turned round to work in English: the altar names are asked for by their initials (S-D-D-P),
  with "Wind-wood-fire" and "Dog-eat-dog" for the two four-kanji sayings among the wrong answers; the
  near-miss spellings of Atamoni, Elraine and Vassago are English near-misses ("Atarnoni", "Elra1ne",
  "Wassago"); the prophet's fishy name gets "Fishy if you ask me".
- Two names were changed elsewhere to agree with the quiz: the sweet shop is "Stall: So Sweet", the
  nickname is "Lewd {NAME}", the cocktail is "Liqueur Sad Love", Nanaly's arte is "Dragon Fire" and the
  dish is "Omurice".

## Open

- A second look on screen (2026-11-23, 03:47 to 04:32 PT, on the full pack) saw whole: the main menu, the
  Enchant and Artes screens with spells in the narrow font, titles, items, a shop and its descriptions,
  the Owlbear's name plate, two skits, a sign, and the first question of a quiz with its four choices.
  It did not reach: the messages of the battle program, recipes, the skit title list, the map's place
  names, a choice window, a long speaker label, or any battle after the first.
- A fill-in quiz (06190 to 06195) takes its answer typed from the name-entry screen's character table,
  so the answer must match the Japanese string and those six cannot be answered in English. The
  questions and replies are English all the same. On that table's hiragana page the first three rows
  show the pack's Latin letters, which took those cells of the font.
- The Custom screen gives a word 14 px a column and draws it at 16 px a letter, so two-letter words
  touched ("NoOn", "BodyFace"). Every option word there but the last of its row now ends in a space
  (`Off `, `On `, `Body `), which gives it room and draws nothing. Seen clean on the real pack at
  05:26 PT, with the Field popup.
- Seen clean at 05:14 PT: the weapon slot as `Wpn.` (the longer word ran into its icon), `Camera L/R`
  (it started on the popup's border), and `Plan` / `Atk` / `Def` on the Tactics party panels (the
  longer words ran into the numbers).
- Six strings were seen whole at 05:26 PT: the quiz picker's "Tales of
  Destiny 2" (06203.6468), Cooking's "Auto (on a tie: … )" (06807.29696; the game centres Food cost,
  Cook count, Aptitude or Any in the gap, and a value of up to 12 letters clears the bracket), and the
  four corner labels of Custom → Menu background (06808.18440 to .18520, "Colors.TopL. R" and so on).
  Such a string holds standard Shift-JIS pairs, which the script files write as `{81}` or `{82}` and
  the next byte.
- "Princess of Mermaid" and "Indignate Judgment" touch if they share a row of the arte grid; whether
  they ever do in play was not checked.
- Seen on screen from power-on: the forest, the flashback, the first battle, Kyle waking and the notices
  in Cresta. Eight skits (00056 to 00066, 00070 and 00074) were seen with every line whole at the faster
  pace. The menus were seen once, before their wording was shortened where labels ran into each other;
  the shortened wording has not been seen. Nothing from Darilsheid to the ending, no later skit, no
  message of the battle program and none of the lists as now written has been seen on screen.
- The other 600 skits pass the build's timing rule but have not been watched.
- Not measured on screen: the names of enchants and recipes, the titles of skits, the names of shops,
  what a recipe says, and the area names at the end of the lists.
- Signs and plaques written with line breaks in the game are mostly written here as one sentence and left
  to the build to wrap. A few keep their breaks (the stone tablets in Darilsheid, the racing results in
  Neustadt, the lists on the altars of the Catacombs); those are the ones to look at first on screen.
- Long speaker labels have not been seen in their plates: "The Man Who Loves Freedom", "Former
  Paratrooper", "Weapon Shop: One Against a Thousand", "Gen the Town Carpenter".
- Not seen yet: the inn's choice window, the name plates "Joe the Flipper" and "Whirlwind Loni", and a
  name followed by `'s`. Skit lines avoid `{NAME}'s` until it has been seen.
- A title, an item or an arte filled into a notice now comes from the translated lists; no such notice
  has been seen on screen with its English name in it.
- The fragments the battle program joins into a sentence ("Slot effect: " + "max HP rose" + ".",
  "'s ", " learnt") were translated without seeing the sentences they make.
- Names taken from the first game's English release are from memory, not checked against it.
- Skit 00064.001 no longer names the Laguna Ruins; the line had to be shortened to fit its time.
- The names of the orphans Rim (リィム), Blue (ブルー) and Jan (ジャン) are readings of the sounds; the
  game gives no spelling.
