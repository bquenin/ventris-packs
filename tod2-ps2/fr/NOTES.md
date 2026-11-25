# Tales of Destiny 2 en français: translator's notes

A French pack in progress. It is machine translated from the Japanese and has not been reviewed by a
human translator. These notes hold what whoever carries it on needs: how far it goes, how the text is
written, the names and terms chosen, and what has been seen on screen.

## Where it stands

- **Translated from the Japanese.** The English pack of this game was open beside it for the spelling
  of names and for what it had learned about the game (how each kind of text is shown, the room each
  has), not as the text to translate. Names of people and places are the English pack's, which are
  readings of the Japanese sounds.
- **What is translated:**
  - the whole story, scripts 06306 to 06790: the dialogue, the captions, the notices, the signs, the
    townspeople, the shops and inns, the lessons one can overhear, the side stories and the ending;
  - the menu screens (06798 to 06816), the messages of the battle program (08055) and of the world map
    (08996), and the enemy names;
  - the lists the menus read (`program.txt`): artes and spells, tactics, enchants, the powers of
    refining, items, valuables, food, cookware, recipes, equipment, titles, shops, the world map's
    places and the short labels of the status screens;
  - all the skits (00056 to 01298) and their titles;
  - of the quiz game: its screens and what its six hosts say (06167 to 06183), four of its six quiz
    books whole (06184 to 06187), and the fifth (06188) up to its offset 14923, with twelve later
    answers that repeat a string written elsewhere.
- **What is not:** the rest of the fifth quiz book, the sixth (06189) and the minigames (06190 to
  06301): about 2,100 strings. They keep the game's own Japanese.
- **Left as the game has them, on purpose:** the seven digits of the Options screen and the two arrows
  `＜` `＞` of a list (they are wide characters in the game, and the Options values overlap when they
  are written as narrow ones); two skit lines whose time on screen leaves room for no letter or for one
  (00856.012, 00926.009); and six answers of the third quiz book (06186) that are one kanji in two
  bytes or two kanji in four, where no French word fits: their questions say what each means (see "A
  quiz string cannot grow").
- **Two parts of this text do not reach the screen with ventris 0.2.0**, in this pack or in the English
  one. The game loads the battle module and the field module from a second, compressed copy that the
  build does not rewrite, so the strings of 08055 and 08996 are in the pack and the game still shows its
  Japanese; and the prompt for leaving a town is a string the build does not yet reach. A correction is
  proposed to ventris (its pull request 15) and is in no release yet. See "What has been seen on
  screen".
- **Read against the Japanese by a second reader.** Every hand-written string of the story, every skit,
  and the quiz text of 06167 to 06186 was read beside its Japanese by an agent that had not written it,
  and its findings were corrected. The fourth and fifth quiz books (06187, 06188) have not had that
  reading.

## How the text is written

- **The apostrophe is `’`** (U+2019), not `'`.
- **No-break spaces.** French puts a space before `?`, `!`, `:`, `;` and `%`, and inside `« »`. In this
  pack each of those is a no-break space (U+00A0): the build breaks a line only at an ordinary space,
  so a mark can never start a line alone. A script puts them in after the text is written. The game's
  narrow font gives every letter the same width, so a no-break space is as wide as a letter.
- **Speech in a bubble has no guillemets**: the bubble and its name plate say who speaks. Guillemets
  are for words quoted inside a line, and for a title or a name the game puts in brackets.
- **Three dots are three full stops** (`...`). The game's own `…` is a wide character with its dots at
  mid-height.
- **Accented capitals are written** (`Épée longue`, `À toi de voir`). ventris 0.2.0 draws them without
  their accent in this game; a correction to the font is on its way to ventris.
- **`HP`, `TP`, `SP`, `LV` and `GRADE` stay as they are.** The game draws them as pictures on the status
  and battle screens, and a pack does not change pictures, so the text says what the screen says.
- **A line of dialogue is written unbroken**; the build breaks it to fit the bubble. In the lists every
  line break is the author's, and each kind has its room: 44 letters on each of 2 lines for an arte,
  39 a line for equipment (2 lines) and items (3 lines), 42 on each of 3 lines for a title, 17 letters
  for the name of an arte, 22 for a piece of equipment, 25 for an item, 28 for a title.
- **The lists share their room.** All the list strings a pack changes must fit in the room the game's
  own took, so the French is written short: no article where a label will do, `Régén.`, `Écon.`,
  `Rés.` in labels.
- **A skit line has a budget of letters.** A skit is voiced and each line stays on screen for a set
  time; with the build option `skit-pace` a changed line is typed faster, down to a floor, and must
  still be whole before the next one pushes it off. So each line may hold so many letters and no more
  (a name tag counts six, whatever the name), and many French lines are shorter than a full rendering.
  The cut was made in the wording, never in the point of the line.
- **Four skit lines write a name in letters** (`Reala` at 00472.003, 00526.006 and 00600.015, `Kyle` at
  00796.004), as the English pack does, because the name tag would not fit the line's budget. One
  line, 00856.012, has a budget of no letters at all and is left as the game has it, as the English
  pack leaves it; another, 00926.009, has a budget of one letter and is left too.
- **A quiz string cannot grow.** Each string of the quiz books has a room counted in bytes, the room its
  Japanese took, and may have no more lines than the Japanese. A French letter costs one byte and a
  Japanese character two, so a question usually fits, written short, and a two-character answer leaves
  four bytes. Where the French word does not fit:
  - a wrong answer gets a short French word of the same kind (`Loup` where the Japanese has a dog,
    `Jade` for a gem, `Pin` for a tall tree);
  - a name of this game that is too long for its room is shortened, and the question carries the rest
    (`Le Héros` for the `Héros voyeur`, with `quel voyeur` in the question; `Gamin Mach` for the
    `Garçon Mach`; `Bon aîné` for the title `Bon grand frère`);
  - an answer that begins with a space in the game begins with one in the pack;
  - an answer that is one kanji in two bytes stays as the game has it, as the English pack leaves it,
    and its question gives the meaning in brackets: `(剣 épée, 盾 bouclier)`, `(蛇 = serpent)`,
    `(海竜 = dragon des mers)`, `(犬 chien, 亀 tortue)`. Four questions of 06186 do this. Their seven
    kanji are the only Japanese characters the pack writes; they are the game's own wide characters
    and take none of the spare cells below.
  Names from the other games of the series are spelled as the English pack spells them, and their
  artes and items have short French names made for the room they have.
- **The letters the pack uses** beyond plain ASCII: `é è ê ë à â ç î ï ô ù û ü œ`, `À Â Ç É È Ê Î Ô Œ`,
  `« » ’` and the no-break space. The game has 80 spare cells for narrow letters and this set, with the
  small letters `a` to `z`, `;`, `~`, `[` and `]`, takes 55 of them. A character outside the set would
  take one more cell, so the checks refuse it.
- **A list to choose from** keeps the wide spaces (U+3000) the game puts around each choice.
- **Button prompts** (`{09:..}` tags) are written without quotation marks: `Maintenir {..}`.
- **`(Chance)` and `(Durable)`** head an effect that comes by chance or lasts a while, where the game
  writes `＜確率効果＞` and `＜継続効果＞`.
- **A name the Japanese repeats is often said once.** Where a line names the person spoken to twice,
  the French says `tu` or `elle` the second time, so the line holds one name tag fewer than the
  Japanese. That is meant.

## What stays in English, and why

- **Spells** (`Stone Zapper`, `Heal`, `Indignate Judgment`): the game writes them as English words and
  the voices call them out in battle.
- **The readings of the artes** (`Sohajin`): the Japanese name in Roman letters, as the voices say it.
  The name beside it is French (`Lame d’azur`).
- **The five grade names of each refining power** (`Power`, `Mighty`, `Welkin`) and the grade names of
  equipment slots (`Attack`, `Veteran`, `Orichalcum`): English words in the game, kept as flavour; the
  line above them says in French what the power does.
- **Names of battle mechanics**: `Spirits Blaster`, `Press Guard`, `Technical Smash`, `Field of Effect`,
  `Guard Strike`, `Battle Grade`, `CHAIN`.
- **Shop names** the game writes in a foreign tongue (`Soul & Sword`, `Blue Lagoon`, `Mahlzeit`).
- **Places the game names in English**: `Heat River`, `Hope Town`, `Trash Mountain`, `Spiral Cave`,
  `Devil’s Reef`, `Aqua Labyrinth`.

## Party

| tag | name |
| --- | --- |
| `{NAME:01 00 00 00}` | Kyle |
| `{NAME:02 00 00 00}` | Reala |
| `{NAME:03 00 00 00}` | Loni |
| `{NAME:04 00 00 00}` | Judas |
| `{NAME:05 00 00 00}` | Nanaly |
| `{NAME:06 00 00 00}` | Harold |

Harold is a woman whom the world takes for a man because of her name; text about her is in the
feminine (`Conceptrice des Swordians`, `Archère` for Nanaly). Until the party meets her, people speak
of `le professeur Harold` in the masculine, as they believe.

## Tu and vous

Japanese marks how formal a speaker is, and French has to choose.

| Who speaks to whom | Form | Why |
| --- | --- | --- |
| The six of the party, to each other | tu | Companions of the road, most of them young |
| Judas | tu to one, vous to several | Curt and formal: `Fâcheux.`, `Sotte question.` |
| Kyle to his mother Rutee | tu, `maman` | His father is `papa` |
| Loni to Rutee | tu | She raised him at the orphanage |
| Kyle and Loni with the people of Cresta | tu both ways, `tantine`, `papy` | They watched them grow up |
| Kyle to grown strangers, to Woodrow, to Philia | vous | A boy speaking politely to his elders; he says plain `Woodrow`, `Philia` |
| Kyle to Nanaly, Chelsea and Fayte to Kyle | tu | Kyle says vous to Chelsea |
| Grown townspeople to Kyle | tu | He is fifteen |
| Shopkeepers, innkeepers, clerics to customers | vous | The Cresta shopkeeper and the cook who teaches recipes say tu |
| Believers and soldiers to Elraine | vous, `dame Elraine` | Philia is `dame Philia` to believers |
| Elraine to the party | vous | To Reala and to Judas she says tu; Reala says tu to her |
| Fortuna to Reala | tu, `ma Sainte` | The party says tu to Fortuna |
| Gaap, Dantalion and the other servants of Elraine | vous, `messire Kyle`, `dame Reala` | |
| Barbatos to everyone | tu | Contempt |
| Harold | tu to one, `vous autres` to several | To her brother's face `frangin`; of him, `mon frère`, `le frangin` |
| Litler, Dymlos, the officers of the past to the party | vous | Kyle calls Litler `commandant`; Dymlos says tu to Harold, Karell and Atwight in private |
| Chaltier to Judas | vous, `jeune maître` | |
| Stahn and Kyle in the ending | tu, `papa` | He is his living father there |
| The menus and tutorials to the player | vous | |
| A character's own words in a title or a description | tu | They speak as they do in the story |

## How people speak

- **Loni**: `Crétin !` for `バカ！` and `Cré~tin !` for `バ〜カ！`; loose negatives (`Cours pas !`). The
  orphans call him `grand frère Loni`.
- **Judas**: short, cold, never slang. `sot`, `idiot` where he insults.
- **Harold**: `T’es bête, toi` (`あんた、アホね`), the laugh `Gnihihi !`, `Gni, gnihihihi !`. Her boast
  `神をも越える` is `surpasse même les dieux` each time she says it: a set turn in the plural, apart from
  the rule about Fortuna below.
- **Nanaly**: plain and warm; `Idiot !` where she scolds.
- **The Katz** end their lines on `, miou`; the kitten on `, miu`, then `, mia` once it has a home.
- **Tics stay with their owner** and are not put on every line: the Rookie (`Bleu`) says `, quoi` and
  `à fond`, the Veteran's father `ma foi`, John `pour sûr`.

## Names and terms

| Japanese | French | Note |
| --- | --- | --- |
| 特技 / 奥義 / 秘奥義 | arte / arte arcane / arte mystique | `un arte`, masculine |
| 術, 晶術 | sort | 下級, 中級, 上級: `sort mineur`, `médian`, `majeur`; 昇華晶術: `sort sublimé` |
| 追加特技, 追加晶術 | arte additionnel, sort additionnel | |
| 通常攻撃 | attaque normale | |
| 術・技 (menu) | Artes | |
| エンチャント | Enchantement | |
| 作戦 | stratégie | `Plan` on the narrow panels |
| リファイン | raffinage, raffiner | |
| スロット | emplacement | |
| 称号 | titre | |
| 料理, 熟練度 | cuisine, maîtrise | |
| 食材 | ingrédients | `Vivres` on the tab |
| 道具 | Conso. (the category), Objets (the battle command and the menu) | |
| ステータス異常 | altération d’état | Poison, Faiblesse, Paralysie, Gel, Lenteur, K.-O. |
| 攻撃, 防御, 命中, 回避, 知性, 幸運 | Attaque, Défense, Précision, Esquive, Intellect, Chance | |
| 詠唱 | incantation | `Vit. sort` as a stat |
| 地 水 火 風 光 闇 | terre, eau, feu, vent, lumière, ténèbres | |
| 硬直 | récupération (one's own), immobilisation (a foe's) | |
| 受身 | rétablissement | |
| 戦闘ランク | difficulté | Its ranks are English in the game and stay so: Easy, Normal, Second, Hard, Mania, Unknown |
| グミ | gelée | `Gelée de pomme` |
| ボトル | fiole | `Fiole de vie` |
| レンズ | Lentille | |
| ソーディアン | Swordian | `l’équipe des Swordians`, `Maître Swordian` |
| ガルド | Gald | |
| ねこにん | Katz | `Village Katz` |
| 神 | la déesse | For believers and for anyone who knows it is Fortuna. `une divinité` only for the being Elraine means to bring down, as the party speaks of it before they know. Never `un dieu`, nor `Mon Dieu` in anyone's mouth |
| 神の力 | le pouvoir divin | `le pouvoir de la déesse Fortuna` where the line is about her own strength |
| 神の眼 / 神のたまご | l’Œil de Dieu / l’Œuf de Dieu | Names of things, as the lists have them |
| 神の降臨 | la descente de la déesse | |
| アタモニ神団 / フォルトゥナ神団 | l’Ordre d’Atamoni / l’Ordre de Fortuna | `la déesse Atamoni`, `la déesse Fortuna`: both are goddesses (the statue in 06392 says so of Atamoni) |
| 司祭 / 神官 / 大司祭 | prêtre / clerc / Grand prêtre | |
| 四英雄 / 英雄王 | les Quatre Héros / le Roi-Héros | |
| 聖女 | la Sainte | |
| 天地戦争 | la guerre du Ciel et de la Terre | `la guerre Ciel-Terre` where a list line has no room |
| 地上軍 / 天上軍, 天上人 / 地上人 | l’armée terrestre / l’armée céleste, les Célestes / les gens de la terre | |
| 総司令 / 中将 / 少将 | commandant en chef / général de division / général de brigade | `le commandant en chef Litler` |
| 地上軍拠点 / 物資保管所 / 作戦室 | Base de l’armée terrestre / Dépôt de matériel / salle d’état-major | |
| 空中都市 / 天空都市 | cité aérienne / la cité des cieux | |
| 蒼天都市, 紅蓮都市, 黄昏都市 | la Cité d’azur, la Cité écarlate, la Cité du crépuscule | Bynames of the cities, capital on the noun |
| 歴史改変 | l’altération de l’histoire | `Le monde altéré` in the skit titles |
| 精神世界 | le monde intérieur | `L’esprit de Kyle` in the skit titles |
| 箱庭 | jardin miniature | Judas's word for the world under domes |
| 出産式 | cérémonie de naissance | |
| 光のほこら | Sanctuaire de Lumière | |
| 飛行竜 / 飛行艇 | Dragon volant / aéronef | The aircraft's name is `Ixifosler` |
| 脱出ポッド | capsule | |
| 制御装置 / 制御室 | dispositif de contrôle / salle de contrôle | |
| 長屋 | maisons mitoyennes | |
| 地下水路 | canaux | |
| ソーサラーリング / ソーサラースコープ | Anneau du sorcier / Lunette du sorcier | |
| モンスター図鑑 / コレクター図鑑 | Bestiaire / Livre du collectionneur | |
| スクリーンチャット | saynète | |
| 蒼破刃 | Lame d’azur | |
| めくりのジョー / 雷光のネルソン | Joe le Trousseur / Nelson l’Éclair | |
| 疾風の, 陽光の, 雷鳴の, 黒衣の, 流星の, ねぐせ | la Bourrasque, Rayon de soleil, le Tonnerre, le Noir, l’Étoile filante, l’Épi rebelle | After the name: `Kyle la Bourrasque` |
| つむじ風の | le Tourbillon | |
| ふられマン / 仮面ストーカー | Râteau-Man / Rôdeur masqué | The running jokes of the skits; the same words in the lists, the skit titles and the skit lines |
| 神経衰弱 (the card game) | le jeu des paires | Its title, 神経衰弱王, is `Roi à bout de nerfs`, to keep the joke about a game that wears out the nerves |
| おにごっこ, 鬼王 | le jeu du loup, Roi-Loup | |
| 姉御, ねーちゃん | Frangine | One word for both: `{NAME} la frangine`, `Frangine Mach` |
| 外殻 | la Coque externe | `Coque` on the world map, where the name has 7 bytes |
| 輝きの聖女 | la Sainte radieuse | Elraine; she is `dame Elraine` to believers, and Philia `dame Philia` |
| 勇者 | preux | Kept apart from 英雄, `héros`, which the story turns on |
| 礼拝の日, 参拝客 | jour de culte, pèlerin | |
| 鍛冶屋 | forgeron | His ranks are in 06353: `Forgeron novice` to `Dieu des forgerons` |
| ネコ好きのじいさん, 命名じじい | le Vieil ami des chats, le Pépé baptiseur | He hands out the epithets below |
| 不死者, 亜人, 甲殻類 | Mort-vivant, Humanoïde, Crustacé | Kinds of monster in the Bestiaire |
| リッチマン (a speaker's label) | Richard | The slang word for a rich man, meant |

People: `Miktran`, `Karell`, `Leon Magnus`, `Barbatos Goetia`, `Litler`, `Dymlos`, `Atwight`, `Clemente`
(`maître Clemente` in address), `Chaltier`, `Woodrow` (`le roi Woodrow`, `messire Woodrow` from Chelsea),
`Johnny` (`messire Johnny`).

Equipment follows the French names of arms and armour where there is one (`Salade` for a sallet,
`Bourdon` for a staff, `Gambison`, `Corsèque`, `Miséricorde`, `Jonc` for a bangle); names out of myth
take their French spelling (`Borée`, `Zéphyr`, `Iseut`) or stay as they are known (`Excalibur`,
`Gungnir`, `Ama no Murakumo`). The weapons and armour named 「グリム…」 share one line: `… de légende, du
nom de frères conteurs.`

Jokes turned round to work in French: the carrot's "foreign tongue" word is the English `carrot`, as in
the game; the failed miso oden ends on `Mystère et soupe miso`; the title 迷探偵 is `Détective privé de
flair`; the mangled title ゾーディアン・マズダー is `Maîdre Zwordian`; Kyle mishears chaos theory as `la
« théorie du K.-O. »`; the proverb ケンカするほど仲がいい is `Qui aime bien châtie bien`; the pun on カイロ
in skit 00198 is made with `cap` and `cape`; Harold's made-up proverb in skit 00704 is `Lézard de Dagno,
serpent de Galua : jamais ensemble`.

## What has been seen on screen

All of it in PCSX2, from power-on, on images built with ventris 0.2.0 from the Japanese disc (version
1.01). **Nothing after the world map outside Cresta has been seen on screen**: the Laguna Ruins and
every later string have only been built and checked by tools. No quiz has been seen on screen.

- **Seen whole and right on a third build**, played from power-on to the world map: Rutee's room and
  the balcony scene, the evening at the table, the night with its choice and the dream, the morning
  with Loni, Rutee in the kitchen, the inn and the grocer of Cresta with the recipe offer, a battle won
  on the world map (two name plates and two items won) and the map's `Entrer` / `Annuler` prompt: about
  110 bubbles more, with no line cut and no mark alone at the start of a line. On a fourth build the
  Options screen was seen right: its values stand apart and its digits are the game's own.
- **Seen wrong on that third build:**
  - Fleeing a battle shows the game's Japanese message, though the pack translates it (08055.340160),
    and the prompt for leaving Cresta reads the French place name followed by Japanese. Both are text
    the build does not put where the game reads it (see "Where it stands"); the pack cannot correct
    them.
  - One line of the balcony scene (06321.092) ended on a page of three words. It has been shortened to
    one page since; that has been built and not seen.
- **Seen on a build made with the correction proposed to ventris** (not released; the pack as it was
  at its first push), from power-on: the battle menu in French, the banner `En fuite...` on fleeing a
  battle, and the menu's location panel `Monde : Seinegald`. So those strings do reach the screen
  once the build writes them where the game loads them. On that build the four labels of the battle
  menu ran into each other: each has a slot of five letters. `Artes` and `Équiper` are now `Arte` and
  `Équip`; that has been built and not seen. Not seen there: the results labels, the message for a
  title earned, what a new arte or lesson says, the other ways a battle ends, the airship's messages.
- **Seen whole and right** on two earlier builds of this pack: the title menu; the opening caption and
  the forest scene; the first battle, an enemy's name plate and the item won; the notices after it; the
  town of Cresta (townspeople, the signboard, the monument, the alarm bell and its choice, an
  overheard lesson with its Oui / Non window, the two men of the epithets); the row house; the shop,
  seen whole, with its buy list and its questions; the talk on the bridge (about thirty bubbles) and the
  orphanage on two floors; three skits (00056, 00058, 00060), each line typed to its end before the
  next; and the menu screens: the main menu, Artes, Enchantement, Stratégie, Cuisine, Options and its
  popups, Objets, Équipement, État, and Sauvegarde (opened only). Across about sixty bubbles of story
  text no line was cut, no mark stood alone at the start of a line and every name plate fitted.
- **Faults seen and corrected**, then seen right on the second build: `Nouveau` cut on the cooking
  screen (now `Neuf`); three strategy names touching their label; `Manteau` and `Vit. sorts` starting
  on a panel's border (now `Mant.`, `Vit. sort`); a label against the edge of an Options popup.
- **Seen wrong on the second build, corrected and then seen right on the fourth:** on the Options screen
  the values of a row ran into each other (`Off` into `On`, `Perso` into `Visage`), and the digit row
  touched. The game places the next value by the bytes of the one before. `Off`, `On` and `Perso` now
  end on a space, as the English pack does, and the seven digits are left as the game's wide ones.
- **Faults seen and still there:**
  - In the Équipement list a slot grade and a kind of weapon are drawn joined, `AttackEpée`: the game
    puts the two words together with no space, as it does in Japanese.
  - Capitals with an accent lose it (`É` shows as `E`), and the hyphen is drawn as the game's long
    minus sign, so `dis-moi` reads `dis–moi`. The first is ventris's to correct.
  - The circumflex of `î` in the small label font is one pixel high; `Chaîne` reads almost `Chaine`.
- **Not reached on screen:** the Laguna Ruins and everything after; the Rune Bottle seller and the
  mystery warrior in Cresta; the table of normal attacks in the lessons (06308.618, which the game plays
  at Aigrette's harbour as 06394.376); the skit list and the skit titles; every skit but three; every
  quiz; Raffinage; the Bestiaire; the status labels `Humanoïde`, `Crustacé`, `Mort-vivant`.

## Open

- Not seen on screen: all the story after the first steps on the world map, all the skits but three,
  the enemy names but three, the skit titles, and all the quiz text. Nothing has shown how a quiz
  question's lines sit in their box.
- The strings of 08055 (battle menu labels, what a new arte or lesson says, the three ways a battle
  ends) and 08996 (names of places on the field, three messages of the airship) are translated and do
  not reach the screen until a released ventris writes them where the game loads them; a few were seen
  right on a build with the correction (see above). The prompt for leaving a town is not in the pack
  yet: its address is one that correction adds. The game writes the place's name into the string at a
  set position, so the French has to begin with the button and the name: the button, the place's name,
  then ` : sortir`.
- The rest of the fifth quiz book, the sixth and the minigames are still to be translated.
- The fourth and fifth quiz books (06187, 06188) have not been read against the Japanese by a second
  reader.
- Quiz answers with four to six bytes of room: the rule in "How the text is written" is one choice
  among others, and where the right answer itself is such a string the player is asked to recognise a
  shorter word than the story's (`Lens` for the `Lentille`, `Mûre` where the answer is purple, `Cof.`
  for a treasure chest). The cure would be for these strings to be able to move.
- The four questions that give a kanji its meaning have not been seen on screen: nothing shows how the
  game's kanji sit inside a French line. The checks report those seven kanji as characters outside the
  pack's set; that is expected.
- About 200 lines of dialogue end on a page that holds only a word or two, where the French runs a
  little past the last full page. They are whole and readable; they have not been reworded.
- The words the program joins into a sentence (`HP ` + a number + ` % rendus`, ` : guérison`,
  ` : plat prêt.`, ` : utilisé`, `il` / `ils` / `elle`) were written without seeing the sentences
  they make.
- The room on screen for the names of enchants, recipes and shops, for what a recipe says, and for the
  labels of the status screens is not measured; the French keeps close to the length of the English
  pack's, which was seen in part.
- The prompts of the Aqua Labyrinth (`Passer au suivant ?`) were written without seeing what "the next"
  is on screen.
