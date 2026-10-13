# Xiaoxiang Realm Expansion — 1.0.1

The curve this mod exists for is now the one it ships with. Everything below
either follows from that or was found while making sure of it.

---

## 🏮 The Nine Heavens preset is the default, and it is a switch

**`[values] nineHeavensPreset`, on out of the box.**

Cultivation is priced in nines, and it is long:

| realm | the whole climb |
|---|---|
| Mortal | 9,999 |
| Qi Refining | 99,999 |
| Foundation Establishment | 999,999 |
| Golden Core | 9,999,999 |
| Nascent Soul | 99,999,999 |
| Soul Formation | 999,999,999 |
| Void Refining | 9,999,999,999 |
| Body Integration | 99,999,999,999 |
| Mahayana | 999,999,999,999 |
| Tribulation Transcendence | 9,999,999,999,999 |

Every realm ten times the one below it, across ninety-nine breakthroughs. **Turn
it off and the original mod's own numbers come back**, scaled by your physique
exactly as they always were, still split into ten layers — nine for Mortal.

**It is one choice with two names.** `nineHeavensPreset` and `useGameNumbers`
are always opposites — turn either one off and the other comes on. They exist as
a pair because people ask the question from both ends: *"give me the long curve"*
and *"give me the original mod back"* are the same decision, and a single switch
can only be named for one of them. Whichever name it got, half the people looking
for it would not find it.

Set both the same way by hand and the file corrects itself within a quarter of a
second. Nine Heavens wins a tie, because a tie broken the other way would quietly
turn the mod off.

**Turning the preset ON rewrites every value on every realm page.** That is what
a preset switch is for. Turning it OFF writes nothing — your numbers stay exactly
where they are and simply stop being read, so flipping back and forth to compare
costs you nothing.

> ⚠️ **If you already installed 1.0.0**, your config file has `useGameNumbers =
> true` written in it and you will keep it. A default only decides what a *fresh*
> file starts at. Set `nineHeavensPreset = true` — or delete
> `xiaoxiang_realm_expansion-common.toml` and let it regenerate — to pick up the
> new curve.

---

## 🌾 Mortal has nine layers and no Peak

**Mortal's ladder is now nine rungs: Early, Middle and Late with three layers
each, and nothing above Late.**

A Peak is worth sitting in because of what it *waives.* In a cultivation realm
the next breakthrough asks for materials, and holding Peak is how you buy time
to go and find them. A mortal has none of that ahead of them — there is no
foundation to lay and no core to form — so a Mortal Peak was a tenth grind that
paid out nothing. **The top of Late is now the top of Mortal.**

Nothing about the price moved. **Mortal still costs exactly 9,999 end to end**
on the Nine Heavens curve; there are now nine ways to divide it rather than ten.
The reward shape follows: **two** sub-stage crossings inside Mortal rather than
three (Early into Middle, Middle into Late), and clearing layer nine is what
leaves the realm.

Every realm above Mortal is untouched — ten layers, Peak included — so the
save-wide figure is **ninety-nine breakthroughs, not a hundred.** Every page,
tooltip and description that said a hundred has been corrected.

**And it is a switch: `[values] mortalPeak`, off out of the box.** The reason a
Mortal Peak pays nothing is a fact about the base mod, not about cultivation —
so if a later version of Xiaoxiang Cultivation World gives one something to
waive, the tenth rung is one tick away instead of one release away. Turning it
on gives Mortal ten layers, three sub-stage crossings, and the tenth rung as the
one that leaves. The price does not move: Mortal's total is divided into nine
parts or ten, so a Peak makes each rung **cheaper** rather than making Mortal
longer. It takes effect on restart, because the layer boxes are built once when
the game starts — and while it is off, Mortal's Peak page is not built at all
rather than sitting there empty.

> 🔍 **Found while checking it:** the code and the written descriptions had
> *already* disagreed about this. `MORTAL_LAYERS` read the ten-layer preset while
> the description checker reported nine — and both passed, because nothing ever
> put the two numbers side by side. The test suite now asserts the layer count,
> the layout and the price together, so the two answers cannot drift apart again
> without something failing.


## 📐 What 1.0.0 actually shipped, and why this is a fix

1.0.0 shipped `curvePreset = "None"` and `useGameNumbers = true`. So a fresh
install cultivated on **the original mod's difficulty**, sliced into ten layers.
Nine Heavens existed only as something you could pick from a dropdown — the
page called it the house curve and nothing made it the house curve.

The figures a fresh config file *did* contain came from four private constants
that matched no preset at all. So somebody who liked what they saw out of the box
had no way to get back to it after experimenting, because it was not on the list
under any name.

Now the default **is** a preset. "Nine Heavens" in the dropdown returns exactly
what a new install started with.

---

## 🧮 A stated total is now honoured exactly

Applying a curve wrote the Peak floor **on top of** the realm's total instead of
inside it. The floor holds Peak at ten times the whole Late stage, and inflating
Peak inflated the realm — so picking Nine Heavens wrote **47,038,175** into a
Golden Core that the preset itself states as **9,999,999**.

The curve on the page and the curve in the file were different curves, and the
page was the one people had read.

The layers are now written from the curve, the stated total is put back, and the
whole thing divides down the way a total you type by hand already does: the floor
folded into the weights, Peak still ten times the Late stage, **and the four parts
adding up to exactly the figure that was stated.**

---

## ✍️ Typing a number no longer gets it overwritten

Typing a realm total releases the original mod's numbers — that is what makes
typing a figure mean it. Releasing them turns the Nine Heavens switch on. And
turning that switch on applies the curve in full.

Left alone, that chain would have handed you the preset's number instead of the
one you just typed — and only on the first edit after switching across, which is
the kind of intermittent behaviour that never gets reported accurately.

The mod now tells the difference between a switch **it** moved and a switch **you**
moved. Only yours applies the curve.

---

## 📄 Licence: All Rights Reserved

Changed from GPL-3.0, and there is now an actual `LICENSE` file — 1.0.0 declared
a licence whose text it did not ship.

In practice it is permissive where it matters:

- ✅ Free to use, for ever, for any purpose, at no cost
- ✅ **Modpacks welcome** — public or private, free or paid, on any platform or
  none. **You do not need to ask.** Credit appreciated, not required
- ✅ Videos, streams, screenshots and articles, including commercially
- ✅ Modify your own copy for your own use
- ❌ Please don't redistribute a modified copy, or publish it as your own work

If you want something that notice doesn't allow, just ask.

---

## 📦 Also in this release

- **A sources jar** comes with every release, and the mod jar now carries
  `ABOUT_THIS_JAR.txt` explaining why a Forge mod decompiles full of `m_280666_`
  names. Neither is obfuscation; both are the reobfuscation step every Forge mod
  goes through.
- **The in-game config screen** gains the Nine Heavens row, with the same written
  explanation every other setting has — what it does, what happens if you turn it
  on, what happens if you turn it off.
- **The preset list in the config file** said there were eight presets and did not
  mention Nine Heavens. There are nine, and the spread between them is about four
  hundred million fold, not four hundred thousand.

---

## 🔁 The page and the game agree

**The Nine Heavens figures printed on the project page and in the Mods screen
are the figures the game uses**, and no page still names a licence the mod has
moved off.

Two things were set right on the way: the Mods screen was quoting two of the ten
realm totals instead of all ten, and the summary ran past CurseForge's limit.

---

## ⬆️ Climbing never steps down

A realm's **first** layer always costs more than the **ninth** layer of the realm
below it, so crossing a boundary is never followed by the cheapest breakthrough
you have had in hours. True at all nine crossings.

**Peak is the deliberate exemption.** Held at ten times the whole Late stage, it
is allowed to tower over the realm that follows - it is the wall at the top of a
realm rather than a step on the way up, and the Peak route exists precisely
because that wall is worth going round.

---

## 🧪 Notes

- Minecraft 1.20.1, Forge. Verified against base mod **0.1.1480**.
- Safe to add to an existing world. Characters already past Mortal keep their
  realm and sub-stage and gain layers from where they stand.
- Every hook is a runtime override. No file of the base mod is modified.
