# Xiaoxiang Realm Expansion — 1.0.0

First release.

Xiaoxiang Cultivation World gives every realm four steps: Early, Middle, Late,
Peak. Four breakthroughs, and between them a long quiet bar. This mod cuts each
of those realms into **ten layers**, gives **Mortal nine of its own**, and hands
you the number behind every single one.

---

## Realms you climb instead of wait through

**Ten layers per realm.** Early, Middle and Late become three layers each, and
Peak is the tenth. Nine small breakthroughs on the way up instead of three long
silences, from Qi Refining all the way to Tribulation Transcendence.

**Mortal gets nine layers too.** Being mortal used to be one flat number — bank
it and you are a cultivator. Now it is a climb with nine steps in it, so the
first hour of the game has the same rhythm as the rest of it. Switch it off and
Mortal goes back to one step.

**Every layer can pay you.** A small lifespan bonus and a Zhenyuan stat point
per layer, both configurable, both off or on per realm. Ninety breakthroughs is
a lot of small rewards if you want them, and zero if you don't.

---

## Mortal pays in the body

Every realm above Mortal rewards a breakthrough with Zhenyuan — points you spend
afterwards on whichever stat you like. **Mortal has no qi to allocate yet.** It
is the body being tempered before there is anything to spend, so it pays
directly: the attribute moves the moment the layer clears, with nothing to come
back for.

- **An ordinary layer raises one attribute.** Rolled from the five, or aimed
  wherever you point it.
- **Crossing into the next Mortal sub-stage raises all five at once** — layer 3
  and layer 6. That is the moment worth waiting for.
- **Leaving Mortal has its own setting**, separate from the crossings, because
  the base mod's own realm reward already lands at exactly that moment.

**Pick a stat, or roll for it.** `focusAttribute` takes `RANDOM` or one of
`CONSTITUTION`, `PHYSIQUE`, `AGILITY`, `SPELL_POWER`, `QI_SEA` — so you can build
a body-tempering mortal before you have cast anything. And `focusChance` decides
how strict that is: 100 pours the whole climb into one stat, 70 sends most of it
there and scatters the rest. (On a server this is one value for everybody, since
it is read from the config file — leave it on `RANDOM` if your players should
choose for themselves.)

**+1 is the default, and it is not the ceiling.** Set the sub-stage crossings to
5, to 90, to whatever a world where Mortal is a serious realm rather than a
prologue needs. Set everything to zero and the layers still work — clearing one
simply moves you along.

**Each layer pays once, ever.** A character demoted back to Mortal climbs it
again and earns nothing again. Otherwise dropping a realm on purpose would be the
fastest way in the game to raise a stat.

Spendable Zhenyuan is there as a setting and ships at **zero**, for anyone who
would rather Mortal behaved like the realms above it.

> **Where:** Expansion → **Layer Rewards** → the three Mortal groups at the top.

---

## Every requirement is yours

**One switch, for all of it.** `useGameNumbers`, under **How Values Work** at the
head of every page. Leave it on and every realm uses Xiaoxiang Cultivation
World's own figures, scaled by your physique exactly as always — the layers still
exist, they just divide the base mod's total. Turn it off and the numbers you
typed take over, everywhere.

A realm's own page is its **total** and the **Sync** button that divides it. Two
rows, nothing else: a switch sitting on top of those was a third thing to
understand before either of the other two did anything, and it was the thing
people missed.

Everything below that switch is a plain number. No checkboxes, no boxes that
save and quietly do nothing because a toggle somewhere else is still on.

- **The whole realm.** "Golden Core should take about fifteen thousand."
- **One sub-stage.** "Golden Core's Late is the wall — four thousand."
- **One layer.** "This exact breakthrough costs seven hundred and seventy-seven."

**The numbers you see are the numbers the game uses.** Set a realm total and
every sub-stage and layer underneath is rewritten to divide it — in the file and
on the screen, within about half a second. Edit a layer instead and the
sub-stage above becomes the sum of its layers, and the realm total follows.
Whichever box you touched last wins, and the page always adds up.

**A Sync button under each total**, for pushing the realm total back down over
layers you have hand-edited. Flip it, the division runs, it flips itself back
off.

**Split evenly or keep the curve.** By default the division follows the curve the
game already uses, so later layers cost more. One switch splits into equal parts
instead: 15,000 across four sub-stages is 3,750, and across three layers is 1,250.

**Nothing moves on its own.** Type 300 into layer 2 and it costs 300, even below
layer 1. If you would rather the ladder tidied itself there is a switch for that
— **Stop Layers Getting Cheaper**, off by default.

**One switch for layers everywhere.** Either every realm is layered or none is.
No world where Golden Core has ten layers and Nascent Soul has four because a
checkbox was missed.

---

## Everything is explained

Every setting in the tab carries its own entry: what it is, what raising it does
to your game, what lowering it does, and words you can search for. So do all
fourteen pages and the tab itself.

Two hundred and two settings, two hundred and two explanations — and no
setting is released without one.

---

## A health bar, for when the hearts stop fitting

Minecraft draws one heart per two health and starts a new row every ten hearts.
Fine at twenty health. At twenty thousand it is rows of hearts climbing the
screen, over the hotbar, over the chat, over most of what you were looking at.

Past a point — 40 health by default, and you can set it — the hearts become a
single bar with the figures written on it, sitting exactly where the hearts were
at exactly their width, so nothing else on your screen shifts. Absorption shows
as a gold strip along the top.

Purely visual, purely local. Nothing about your health changes, and nothing a
server can see.

---

## Peak is a road, not a wall

Breaking through a realm normally means gathering what the breakthrough asks
for — zhuji pills, blood pills, dao fruit, a secret manual. Fine when the loot
is kind. Less fine when you have been sitting at Peak for three hours opening
chests.

**So cultivate through Peak instead.** Clear a realm's Peak layer and the Human,
Blood and Earth foundations open without their materials. Heaven stays behind
its materials by default, because a route that hands out the best foundation for
time spent would make gathering pointless rather than optional — switch it on if
that is the world you want.

**Peak is priced to match.** It is held at **three times the ninth layer** by
default, so the two roads cost about the same amount of play. Gather, or
cultivate. Never both. The multiplier is a setting, and so is the whole route.

---

## One number, if you want it that way

There is also a mode for people who would rather not fill in ninety boxes. Give
it **one seed number and three growth rates** — how much a layer climbs, how
much a sub-stage climbs, how much a realm climbs — and it works out the entire
curve from Qi Refining layer 1 to Tribulation Transcendence Peak. Anything you
have typed by hand still wins over it, so you can take the curve it
works out and fix the three places you disagree with.

---

## Where you set all this

Thirteen pages inside the config screen, one per realm plus Mortal, the Peak
route, the layer rewards and the seed-and-rates mode. Each realm's page holds
its own tiers — the whole realm, then Early, Middle, Late and Peak — and nothing
from any other realm. No page asks you to scroll past thirty near-identical
rows to find the one you came for.

This needs **Xiaoxiang Config Extension** to be the pretty version. Without it,
everything above is still fully editable by hand in
`xiaoxiang_realm_expansion-common.toml`, and every setting in that file carries
a plain-English explanation of what it does and what happens if you raise or
lower it.

---

## Compatibility

- **Requires:** Xiaoxiang Cultivation World, and Minecraft Forge for 1.20.1.
- **Optional:** Xiaoxiang Config Extension. Genuinely optional — the mod loads
  and plays perfectly without it.
- **Touches no base mod file.** Everything is applied at runtime. Remove this
  mod and the game is exactly as it was.
- **Existing saves are safe.** Every setting ships at a default that changes
  nothing, with one exception: Peak is now held at three times the ninth layer,
  so Peak costs more than it used to. Turn off the Peak floor to undo that.
