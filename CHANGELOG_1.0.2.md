# Xiaoxiang Realm Expansion — 1.0.2

Spiritual water grew up. It has grades now, it will not mix with the sea, you can
make it, and it flies.

---

## 🌊 Six grades of spiritual water

**Inferior, Low, Mid, High, Top, Supreme.** What you had is Inferior and keeps
every one of its numbers. Each grade above it doubles the qi the water gives,
adds one to the strength of its effects, and reaches ten blocks further as a
Blessed Land — up to eighty blocks at Supreme.

| grade | qi | reach as a Blessed Land |
|---|---|---|
| Inferior | ×1 | 30 |
| Low | ×2 | 40 |
| Mid | ×4 | 50 |
| High | ×8 | 60 |
| Top | ×16 | 70 |
| Supreme | ×32 | 80 |

Grades do not mix with each other. One supreme bucket cannot raise a lake and
one inferior bucket cannot ruin a supreme pool; a pond is one grade, and a
mixed puddle is two ponds.

## 💎 How you make it, and how you raise it

**Pour a bucket of water into a one-block hole and throw in a full stack of
supreme spirit stones.** They dissolve over three seconds — bubbles, motes and a
chime — and the water is spiritual water.

**Throw more stone into spiritual water and it climbs.** Any grade of spirit
stone counts here, a stack at a time, and the grade of the stone is roughly the
grade of the water it buys: a stack of mid stone buys Mid, a stack of high stone
buys High, a stack of supreme stone climbs to Top. Whatever a stack does not
spend is kept against the next step. Water already at Supreme refuses the stones
rather than eating them.

**On a crafting bench**, a water bucket and a full stack of supreme spirit stones
make a bucket of spiritual water. Exactly one stack — the recipe will not take
sixty-three.

## 🧱 Water will not mix with it

Ordinary water treats spiritual water as ground. Pour water beside a spiritual
pool at a higher level and it spreads *over* the pool rather than into it, and
nothing falling from above displaces it — so a spiritual spring can sit at the
bottom of an ocean and still be a spiritual spring. Pouring a spiritual bucket
into the sea still works; that is how you put one there.

## 🪣 The Spiritual Vessel — Bucket

A bucket that holds **four buckets**, as a real fluid container any pipe or tank
can fill and drain. It never reverts to a bucket. Its capacity **doubles every
three days you carry it**, eight times at most, to 1,024 buckets. Ordinary water
poured into it **turns spiritual after two days**. The fill level draws in the
durability bar — jade for spiritual water, blue for water that is still turning.

**You earn it, not craft it.** An ordinary bucket that holds spiritual water for
four days becomes a Spiritual Vessel, with the water still in it. A bucket in a
chest counts the same days as one in your hand.

**And it flies.** A sword-flight technique carries you on a Spiritual Vessel as
it would on a flying sword. It is not a weapon — no damage, no enchanting, no
durability.

## ✨ Spirit Obsidian

Spiritual water meeting lava makes jade **Spirit Obsidian** instead of the
ordinary kind. Diamond pickaxe to mine, like obsidian.

## 🔮 A Qi Absorption icon

Standing in spiritual water, or on blessed land, now shows a **Qi Absorption**
effect beside Regeneration and Haste, so the thing the water is for has a face.

## 🏔️ Mortal Peak is a switch

`[values] mortalPeak`, off out of the box. Off, Mortal is nine layers and the
top of Late is the top of Mortal. On, Mortal gains a tenth rung like every realm
above it. The price does not move — Mortal's total divides into nine parts or
ten. Takes effect on restart, and while it is off the Peak page is not built at
all rather than sitting there empty.

## 🐛 Fixed

- **The Blessed Land dome and aura failed most of the time.** The search that
  finds a Blessed Land stepped over the player's own height and only looked at
  every fourth block up and down, so a real nine-by-nine pond was missed about
  seven times in ten. It now checks every height.
- In single-player, a half-loaded measurement taken by the client could be
  served to the server as the truth for three seconds, dropping a grade. Each
  side now keeps its own.
- Stepping out of your own pool could leave you without the aura for ten
  seconds. Fixed.
- The dome's motes were spaced for a thirty-block ring; a larger ring now gets
  more of them, so an eighty-block dome is still a dome.
