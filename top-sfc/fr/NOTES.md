# Tales of Phantasia en français: translator's notes

A first part of a French pack, started to show a second language working in ventris. It is machine
translated from the Japanese and has not been reviewed by a human translator. These notes hold what
whoever carries it on needs: how far it goes, how the text is written, the choices made so far, and
what has been seen on screen.

## Where it stands

- **What is translated:** the dialogue of the opening of the game, sections 01, 03, 05, 07, 09 and 11:
  175 strings. That is the hunt in the forest, the village of Toltus, the attack, the manor and the
  escape, and the last scenes of the game, which share section 11 with the village.
- **What is not:** the other 44 dialogue sections, the menus (`menu.txt`) and the captions
  (`captions.txt`). They keep the game's own Japanese, so an item's name inside a French sentence is
  still Japanese (`Obtenu : アップルグミ.`), and so are the names in menus and battles.
- **Names:** `names.txt` gives the five party members the same names as the English pack. Dialogue
  shows them. The menus keep the game's names until `menu.txt` is translated, because the menu font
  has no free tile before then; the build says so.
- **Translated from the Japanese.** The English pack was open beside it for names and for what it
  had learned about the game, not as the text to translate. Two complete French fan translations of
  this game exist, by Terminus Traduction (2002) and Final Translation (2011), both made from the
  English fan translation; nothing in this pack comes from them.

## How the text is written

The rules of the English pack's notes hold here too: speakers on a line of their own, a party member
as their tag, tags kept as the game has them, a paragraph as one line that the build wraps, a string
that ends with `{PAGE}` ending with it. What is particular to French:

- **Speech is in guillemets**, `« ... »`, with a no-break space inside each. Thoughts are in
  parentheses. A sign or a grave is introduced with `On peut y lire :`.
- **No-break spaces.** French puts a space before `?`, `!`, `:` and `;` and inside guillemets. In
  dialogue these are no-break spaces (U+00A0): the game draws one as a narrow space and never breaks
  a line at it, so a `?` or a `»` cannot start a line alone. A script put them in after the text was
  written; text written with ordinary spaces there is wrong and will break badly.
- **The two lines shown as sprites**, `01.004` and `07.000`, are the exception: no guillemets, and
  ordinary spaces. The page holds 32 letters and the build breaks the rows at spaces; guillemets
  would cost two letters, and a no-break space there has not been seen drawn.
- **Receiving an item** is `Obtenu : {STR:..}.` The name comes from the game's item list, so its
  gender is not known where the sentence is written, and this form needs no article.
- **Accented capitals are written** (`À mains nues`, `Épée longue`). Dialogue draws them correctly.
- **Place names hold 16 characters.** The name of a place or a shop shown in the box at the top of
  the screen is centred by counting its characters, and a longer one is not drawn at all. From ventris
  0.2.0 the build refuses a longer one. A party
  member's name counts as its letters and one more. So: no guillemets, and the short form:
  `Village Toltus`, `Chez {クレス}`, `Église St-Lenios`, `Armurerie Teasel`, `Auberge Le Repos`,
  `Bazar Gori`. In these six sections the place names are `03.000` and `05.000` to `05.005`.
- **Leading lines.** `09.006` starts with three empty lines where the game has three lines holding a
  wide space each, as the English pack does.

## Tu and vous

Japanese marks how formal a speaker is, and French has to choose. The choices so far:

| Who speaks to whom | Form | Why |
| --- | --- | --- |
| Cress and Chester, to each other | tu | Childhood friends |
| Cress to Mint | tu | He says 君 from the first line |
| Mint to Cress, and to others | vous | She speaks politely to everyone |
| Cress to his master Tristan, to Claus, to strangers | vous | He speaks politely to his elders |
| Tristan, Miguel, Maria, villagers to Cress | tu | Elders to a boy they know |
| Chester to Maria | vous | A friend's mother |
| Claus to the younger members | tu | |
| Arche to the others | tu | Casual speech |
| The captors to Cress | tu | Contempt |
| Cress to his parents | tu, `papa`, `maman` | |

## Names and terms

Names of people and places are the English pack's, which are the sounds of the Japanese: Cress, Mint,
Arche, Chester, Claus, Albane, Barklight, Miguel, Maria, Ami, Tristan, Lenios, Martel, Toltus,
Euclid. The French terms chosen so far:

| Japanese | French | Note |
| --- | --- | --- |
| 記憶陣 | cercle de mémoire | |
| 法術 | arts de guérison | Mint's arts; the English pack has "healing arts" |
| 技 / 魔法 | techniques / sorts | In the test messages of section 03 |
| 時間の剣 | Épée du Temps | |
| ガルド | Gald | The currency, unchanged |
| ペンダント | pendentif | |
| 師匠 / 先生 | maître | `maître Tristan`, `maître Albane` |
| ブッシュベイビー | galago | The animal; the statue at the inn |
| 置物 | bibelot | |
| 雑貨屋 | bazar | |
| 受付嬢 / お手伝い / シスター / 神父 / バイト / 主人 | Réceptionniste / Servante / Sœur / Prêtre / Employé / Patron | Speakers written in plain words |

## What has been seen on screen

Built with ventris 0.1.0 from the Japanese cartridge and looked at in Mesen, from power-on.

- **Seen, and right:** about twenty boxes of dialogue in the village and on leaving it, from strings `03.014`,
  `03.015`, `03.022`, `03.024` to `03.026`, `05.045` to `05.047`, and in the forest `01.010`,
  `01.011` and `01.013`. Accents, guillemets and the narrow spaces are drawn correctly, no line runs
  past the box, and no mark is left alone at the start of a line. The speaker's name is drawn from
  `names.txt`. A full three-line page scrolls out line by line after a button press.
- **A fault found there and corrected:** `03.000` as `Village de Toltus`, 17 characters, showed
  leftover tiles in place of the name. That is how the 16-character rule above was found. `03.000`
  and `05.000` to `05.005` were then shortened.
- **The seven place names, seen and right:** `03.000` `Village Toltus` on leaving the house, and
  `05.000` `Chez Cress`, `05.001` `Chez Chester`, `05.002` `Église St-Lenios`, `05.003`
  `Armurerie Teasel`, `05.004` `Auberge Le Repos` and `05.005` `Bazar Gori` on walking into each
  building, every one in its own run from power-on. Each is drawn whole, with its accent, and none
  runs past the box. Names in narrow letters stand left of the middle of the box; the 16-character
  ones start at its left edge.
- **Not seen:** the tree scene of section 01 (the sign `01.000`, the exchange `01.001` to `01.009`,
  the sprite line `01.004`): the forest was walked past the boar and a battle to a clearing with a
  sign in the north, and the scene did not start there. Nothing of sections 07, 09 and 11. A box
  longer than three lines has not been seen either.

## What a complete pack will meet

From a check made with a few French strings in each kind of text, before this pack was started:

- **Menus:** every French letter can be added to the menu font once the naming screen's letter grid
  is rewritten, as the English pack does. Accented capitals are hard to read there (`É` reads as
  `E`), and the plain apostrophe `'` draws better than `’`.
- **Captions:** small letters are right. Accented capitals lost the top row of their accent in ventris
  0.1.0, so `É` read as `È`; ventris 0.2.0 draws the whole accent. A no-break space costs a full letter
  there.
- **Length:** French runs longer than English. The menus' columns (8 letters for an item, 3 to 5 for
  a label) and the captions' 30 letters a line will need shorter words and more moved labels.
