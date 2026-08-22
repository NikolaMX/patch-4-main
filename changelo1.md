# Sunrise — Full Unit Diff vs. Legion Expansion

Every entry below is a difference between the stock **Legion Expansion** unit JSONs and the **Sunrise** (`patch-4-main`) overrides. Only files under `pa/units/` were compared; models, effects, sounds, icons and bone/socket rewiring are summarised at the bottom rather than listed value-by-value.

---

## 🏗️ Economy & Factories
*   **Foundry build rates (all tiers cheaper):**
    *   **Walker / Armour Foundry:** Metal 17 -> **15**; Energy 765 -> **675**.
    *   **Advanced Walker / Armour / Flyer Foundry:** Metal 50 -> **45**; Energy 1650 -> **1500**.
    *   **Advanced Ship Foundry:** Metal 65 -> **60**; Energy 1900 -> **1750**.
*   **Power Catalyst:** Energy production 600 -> **700**.
*   **Advanced Power Catalyst:** Cost 2500 -> **2800**. Health 2500 -> **2000**. Energy production 6000 -> **9000**. Larger footprint (25 -> 30).
*   **OmniSilo Storage Device:** Health 5000 -> **7500**. Energy storage 225,000 -> **75,000**. Death explosion 1200 -> **500** damage. Footprint shrunk 28 -> 20.
*   **Mass Extractor:** No longer lists the Bug advanced extractor as a replaceable unit.

---

## 🔨 Fabricators
*   **Fabrication Walker (Bot Fab):** Health 65 -> **30**; gains a **30 HP personal shield** (30 e/s, 1.5 recharge, 10 s cooldown). Speed 14 -> **15**. Description now "Shielded Builder".
*   **Advanced Fabrication Walker:** Cost 2000 -> **1900**. Health 150 -> **400**. Speed 14 -> **10**. Build energy 2200 -> **1900**. Now has death effects.
*   **Armour Fabricator (Vehicle Fab):** Cost 200 -> **250**. Health 185 -> **200**. Speed 11 -> **10**. Build arm 13 metal / 850 energy -> **16 / 1100**.
*   **Advanced Armour Fabricator:** Health 500 -> **200**. Speed 10 -> **16**. Build metal 70 -> **60**.
*   **Guardian (Combat Fab):** Cost 350 -> **250**. Build arm 45 metal / 600 energy -> **30 / 400**.
*   **Fabrication Flyer:** Health 165 -> **85**. Smaller mesh bounds.

---

## 🛡️ Defense & Structures
*   **Liberator (NEW turret):** Legion's unused scout turret is now registered and buildable — cheap perimeter defense with long sight.
*   **Reclaim Turret (NEW):** Automated wreckage clearing — reclaim-only build arm (30 metal / 400 energy, 200 range), no repair, restricted to `Wreckage` and `Feature`.
*   **Jackal:** Cost 325 -> **275**. Health 750 -> **1000**.
*   **Scarab:** Cost 550 -> **450**. Health 2500 -> **3000**. Range 110 -> **120**. Smaller footprint.
*   **Rampart (Shield Generator):** Health 750 -> **1500**. Now uses a real **shield component**: 15,000 shield HP, 100 radius, 6000 e/s demand, 200 recharge, 30 s cooldown, requires efficiency. The old long-range interceptor tool was removed; the anti-projectile pool was raised 36k -> **60k** ammo with 1000 -> **1200** demand. Footprint halved 30 -> **15**. Leaves 40% wreckage.
*   **Shredder (AA Turret):** Now carries `UNITTYPE_CombatFabBuild` — buildable by the Guardian.
*   **Radar:** Health 500 -> **750**. Vision/radar radius 100 -> **200**. Much smaller footprint.
*   **Hive:** Gains a dedicated **reclaim arm** (auto-reclaim, 60 metal/s, 180 range, assist-restricted) on a rear turret bone, and its main weapon now auto-reclaims.
*   **Barricade:** Legion's **Clot** renamed to **Barricade**. Area-build separation 1 -> **1.2**.

---

## 🚜 Land Units

### Combat
*   **Predator (NEW T1 Vehicle):** 100 metal | 100 HP | speed 15 | 150 accel/brake | 180 turn | 130 vision | `CannonBuildable`.
*   **Lancer:** Cost 150 -> **125**. Health 100 -> **70**. Damage 166 -> **225**. Range 70 -> **80**. Rate of fire 0.61 -> **0.4**.
*   **Peacekeeper:** Health 170 -> **60**, plus a **35 HP personal shield** (15 e/s, 2.5 recharge, 10 s cooldown). Movement `amphibious` -> **`land-small`**. Range 70 -> **67.5**. Vision 105 -> **115**. Now flagged `UNITTYPE_Shield`; requires 90% energy efficiency.
*   **Stoke (Rework -> Anti-Air):** Description now "Anti-Air Tank — armed with a single flak cannon". Cost 210 -> **170**. Speed 14 -> **16**. Damage 39 -> **50**. Range 80 -> **100**. Targets **air only** (land/sea/seabed layers removed). Turret pitch rate 120 -> **360**, yaw rate 160 -> **360**. The shell is now a staged, gravity-free flak round (velocity 200 -> **250**, 15 s lifetime, 20 cruise height) that prioritises transports, bombers, gunships, titans and airborne energy producers.
*   **Patriot (Rework):** Homing missiles replaced with a **4-round laser burst** — per-shot damage 25 -> **7.5** (x4) with 1-radius splash, velocity 200 -> **280**, lifetime halved. Acceleration/brake 120 -> **30**, turn speed 720 -> **360**. Slows to 50% speed while targeting and firing, and stops pushing allies. 3° spread.
*   **Orbweaver (Advanced AA Walker):** Health 400 -> **480**.
*   **Enforcer:** Speed 12 -> **15**. Range 100 -> **95**.
*   **Maul:** Cost 300 -> **170**. Health 1150 -> **600**. Rate of fire 1 -> **0.5**.
*   **Shank:** Damage 125 -> **130**. Splash damage 20 -> **60**, splash radius 5 -> **3**. Shell is now a proper projectile (gravity 5, may pass underground).
*   **Corsair:** Cost 300 -> **220**. Health 175 -> **100**. Rate of fire 0.25 -> **0.3**. Shell reworked into a **staged lofted missile** (cruise height 60, thrust plus terminal homing, 70/50 stage turn rates), initial velocity 200 -> **120**, max 400 -> **50**, gravity 6 -> **10**. Splash 40 -> **30**, radius 10 -> **8**. Now prioritises surface defenses, defensive structures and commanders. Default firing pitch -65°.
*   **Panzer:** Weapon now targets **Air and Orbital only** (Land and Water Surface removed) and takes the same defense/commander priority list.
*   **Miniman:** Ammo capacity 7 -> **8**. Its bombs lose their structure bonus — `AT_Structure` multiplier 3.0 -> **1.0**.
*   **Purger:** Cost 50 -> **60**. Attack range fraction **0.8**; no longer maintains a priority target. Bomb rebuilt on the seeking-missile base — damage 450 -> **334**, initial velocity 80 -> **150**, lifetime 30 -> **1**, 60 turn rate (it now tracks), no structure bonus. The weapon draws **10 energy per shot**; the jump tool auto-attacks and no longer blocks while busy.
*   **Monstrosity:** Speed 12 -> **15** (acceleration 10 -> 15). Vision 100 -> **150**. Range 170 -> **140**. Now prioritises advanced units, tanks and structures over walls.
*   **Deathmark:** Cost 1200 -> **1000**. Per-shot damage 1000 -> **500**; shell velocity 200/500 -> **100/300**, gravity 26 -> **20**. Weapon converted to a **carpet-fire burst** — rate of fire 0.142 -> **10**, fed by a 7-round, time-refilled magazine that waits for a full load. Prioritises advanced units, tanks and structures; no longer maintains a priority target.
*   **Havoc (Rework):** Timed electric mines replaced with **chain lightning** — the bolt jumps up to **2** extra targets within **50** range for **500** damage each, with no falloff. Direct damage 750 -> **500**; projectile speed 200/300 -> **100/150**. The old secondary beam / missile-intercept tool was removed.
*   **Earthshaker (Rework -> Bubble Shield):** Weapon removed entirely; it is now a mobile **shield generator** — 5000 shield HP, 75 radius, 2000 e/s, 300 recharge, 10 s cooldown, 90% efficiency required. Cost 1800 -> **1400**. Health 7000 -> **2000**. Turn speed 180 -> **60**. Flagged `UNITTYPE_Shield`.
*   **Scorpion:** Cost 900 -> **1100**. Health 1650 -> **2000**. Damage 500 -> **750**. Splash damage 150 -> **250**, splash radius 15 -> **5**. Rate of fire 0.4 -> **0.6**.
*   **Necromancer:** Projectiles per fire 7 -> **14** (seven new drop bones). Ammo capacity / cost per shot 420 -> **750**, demand 35 -> **45**. Now transportable (size 1).
*   **Investigator (Scout):** Cost 150 -> **100**. Vision 150 -> **200**. **Radar mode fixed** — radar radius 0 -> **75**, energy draw 100 -> **200**.

---

## ✈️ Air Units
*   **Nova (Rework):** Cost 180 -> **200**. Health 180 -> **150**. Guard radius 0 -> **160**. Trigger range 10 -> **50**, and it will now engage while busy. Spawns its bomb with inherited velocity.
    *   **AOE Nova (the triggered bomb):** Health 500 -> **220**, and it now **flies at speed 130** to chase its target (it was stationary), with a 1-tick target refresh and 160 guard radius. Its weapon becomes a **self-destruct** with full 360° arcs, range 80 -> **5**, prioritising mobile air. The lingering pulse ammo is zeroed out (6 damage / 80 splash -> **0**) and the death blast carries the payload instead: damage 35 -> **150** with **150 splash** over 15 radius (was 6 over 70), damage volume 5 -> **20** radius firing almost instantly (1 s -> 0.01 s delay). Death weapon ammo 20 -> **15**. Leaves no wreckage.
*   **Meteor:** Health 2000 -> **750**. Now circles engaged targets (`circle` behaviour, 230 aggressive distance, 10–20 s circle time, bank factor 2).
    *   **Meteoroid drones:** Speed 80 -> **40**, turn 240 -> **120**, and they can **no longer target air**.
*   **Scythe:** Cost 240 -> **200**. Damage 29 -> **35**. Turn speed 300 -> **240**. Rebuilt on the fighter-turret base: **forward-fixed guns** (yaw range 70 -> **0**), firing arc 70 -> **60**, pitch rate 360 -> **3600**, range 110 -> **107.5**.
*   **Dauntless:** Speed 75 -> **80** (acceleration 75 -> 80, brake 20 -> 25). Bomb velocity 40 -> **25**, full-damage splash radius 2 -> **1**. Ammo capacity 425 -> **424** (one bomb per pass).
*   **Firebird:** Rocket range 180 -> **160**, rate of fire 0.33 -> **0.25**.
*   **Lockheed (Rework):** The **rockets** are now the primary weapon and the gun is secondary — gun range 80 -> **60**, rate of fire 4 -> **2**. Rockets: damage 250 -> **85** but they gain **85 splash over 5 radius**, ammo capacity 5 -> **10**, ammo per shot 2.5 -> **3**, rate of fire 2.5 -> **5**, range 100 -> **60**, spread 30 -> **5**, fired from a single bone with full 180° traverse instead of a six-tube salvo, and they no longer turn in flight. No longer maintains a priority target.
*   **Marauder:** Health 50 -> **40**. Speed 100 -> **90**. Weapon now runs on a **6-round, time-refilled magazine** (1/s regen), so sustained fire falls off. Prioritises fabbers, then anti-air, then land and naval mobiles. No longer maintains a priority target. Fires from a single muzzle.
*   **Osprey (Transport):** Cost 100 -> **165**. Health 55 -> **50**. Speed 100 -> **85**, brake 40 -> **80**. Vision 70 -> **120**. Explicit 15 load range. Re-tagged `UNITTYPE_Offense`.
*   **Comet:** `UNITTYPE_FabAdvBuild` -> **`UNITTYPE_FactoryBuild`** — no longer buildable by fabbers. Lost `ORDER_SpecialMove`. Leaves 50% wreckage.
*   **Infiltrator:** Re-tagged with `UNITTYPE_Offense`.
*   **Salamander:** Spec moved onto a rebuilt `l_bomber_heavy` chassis (new model and assets). Speed 40 -> **60**.
    *   **Purifier (dropped flame turret):** Rebased onto the new chassis, footprint shrunk 10x10x8 -> **3.5x3.5x5**, single muzzle, and it now accepts `ORDER_FireSecondaryWeapon`.
*   **Loki (Titan, Rework):** All four turrets now share one **tripod laser** weapon instead of the split main and side cannons.
    *   New weapon: **100 damage plus 50 splash over 3 radius** per bolt, 700 velocity, 10 shots/sec carpet fire from a 10.1 ammo pool (0.2 per shot, 1/s refill — roughly a 50-shot burst then a reload), range **140** (was 150), 45° pitch / 180° yaw, 5 s idle aim delay, spread fire.
    *   Targets **land, seabed and water surface only** — Air and Underwater dropped from the old main cannon.
    *   Priorities: advanced mobiles, then commanders, then non-air mobiles, then structures, then walls.
    *   Old side-gun splash tightened: full-damage radius 20 -> **5**, splash radius 25 -> **5**.

---

## 🚀 Orbital
*   **Viper:** Damage 40 -> **50**. Range 200 -> **100**. Engages at 75% of max range.
*   **Paladin:** Engages at 90% of max range.
*   **Starcannon:** Stored units are now **visible** on the platform, with 14 real spawn bones instead of one shared bone. Drop scatter 30 -> **50**. Strategic icon priority set to 4.
*   **Starship Projector:** Units now spawn from the shell socket instead of the platform bone.
*   **Centurion:** Leaves no wreckage. (Sunrise also ships an alternate `l_deffense_satelite` folder with a long-range manual-fire ground weapon, but nothing references it — the live Centurion still uses Legion's specs.)

---

## 🌊 Sea
*   **Talos (AA Frigate, Rework):** Beam replaced with **laser-blast rounds** — damage 20 -> **10** but with 10 splash over 1 radius, 280 velocity, 0.7 s lifetime. Range 180 -> **110**, rate of fire 1 -> **2**, yaw 180 -> **360**, pitch 180 -> **90**, spread fire enabled, 3° deviation, no idle aim delay. **Target layers now include `WL_AnySurface`** alongside air.

---

## 🧩 Unit List & Registration
*   **Added:** Predator (`l_attack_vehicle`), Liberator (`l_scout_turret`), Reclaim Turret (`l_turret_reclaim`) — all now in `unit_list.json` and `unit_list_legion.json`.
*   **Removed from the unit list:** `radar_jammer`, `tank_jammer`, `orbital_mine`, `tank_anti_nuke`.
*   **Note:** `unit_list.json` also references `/pa/units/land/l_tank_adv_support/l_tank_adv_support.json`, which does not exist in the mod.
*   **Commander base spec:** now carries `UNITTYPE_Fabber`.

---

## 🎨 Visuals & Plumbing
*   **New or replaced models and animation trees:** Flyer Foundry, Advanced Flyer Foundry, Armour Foundry, Advanced Armour Foundry, Scythe, Dauntless, Fabrication Flyer, Marauder, Lockheed, Salamander and Purifier, Loki, Corsair, Panzer, Scorpion, Shank, Stoke, Radar, Deathmark, Shield Generator, Storage, Mass Extractor, Teleporter, the fabricator line, Firebird and the whole Nova family.
*   **Effects rewiring:** Legion's per-unit jet and contrail PFX consolidated onto shared `l_base_flyer` effects (`jet.pfx`, `jet_small.pfx`, `thrust_line.pfx`, `wing_tip_line.pfx`); factories moved to `legion_fab_spray.pfx` plus dedicated smoke specs; new `energy_ball` / `target_fire` effects for the Nova and `electrode.pfx` for Havoc's chain lightning.
*   **Lighting:** Foundry headlights and lamps re-bound to real alarm bones with new amber and white colours instead of hard-coded offsets.
*   **Bone and socket renaming** across most reworked units (muzzles, thrusters, fabber arms) to match the new meshes; several units also had `attachable` head offsets and `mesh_bounds` retuned to the new models.
