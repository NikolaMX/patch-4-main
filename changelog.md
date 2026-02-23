# Legion Mod Update - Comprehensive Changelog

This update represents a major balance pass and content overhaul for the Legion expansion. Key focuses include a rework of factory efficiency, significant identity shifts for air units like the Lockheed and Marauder, and a role-reversal for the Stoke into a dedicated Anti-Air platform.

---

## 🏗️ Economy & Factories
*   **Factory Efficiency:** Most foundries now consume fewer resources to produce units, allowing for more expansive early-game growth.
    *   **Armour / Walker Foundries:** Reduced Metal rate from 17 to 15; Energy rate from 765 to 675.
    *   **Advanced Armour / Walker / Flyer Foundries:** Reduced Metal rate from 50 to 45; Energy rate from 1650 to 1500.
    *   **Advanced Ship Foundry:** Reduced Metal rate from 65 to 60; Energy rate from 1900 to 1750.
*   **Legion T1 Air Factory:** Production cooldown increased from 2s to 4s.
*   **Starship Foundry:** Build cost decreased from 6000 to 4200.

---

## 🛡️ Defense & Structures
*   **Clot (Legion Wall):** Metal cost increased to **50**.
*   **Liberator Recon Turret (NEW):** Cheap source of true vision.
    *   75 Metal | 150 HP | 230 Vision.
    *   Weapon: 90 Range, 20x2 Damage, 1 RoF.
*   **Reclaim Turret (NEW):** Automated wreckage clearing.
    *   375 Metal | 1000 HP.
    *   **Restriction:** Can ONLY reclaim wreckage (cannot reclaim trees or living units).
*   **Jackal:** Cost decreased 350 -> 275; Health increased 750 -> 1000.
*   **Scarab:** Cost decreased 550 -> 450; Health increased 2500 -> 3000; Range increased 110 -> 120.
*   **Shield Generator:** Health 750 -> 1500; Ammo capacity 36k -> 60k; Ammo demand 1000 -> 1200.
*   **Radar:** Health 500 -> 750; Vision radius 100 -> 200.

---

## 🚜 Land Units

### Fabricators
*   **Fabrication Walker (Bot Fab):** Health set to **65**. Speed reduced to 14. Metal rate 10.
*   **Armour Fabricator (Vehicle Fab):** Health set to **200**. Speed increased to 12. Cost set to **250**. Buildarm set to **16** / **1100**
*   **Guardian (Combat Fab):** Metal cost reduced to 250. Now capable of building **Shredders**, **Liberators**, and **Reclaim Turrets**.
*   **Advanced Fabrication Walker:** HP increased to 400. Cost reduced to 1900.

### Combat Units
*   **Predator (Experimental T1 Vehicle):**
    *   Cost: 100 | HP: 85 | Speed: 15 | Range: 80 | Damage: 40 | RoF: 0.6.
*   **Lancer:** Rebalanced as a high-damage glass cannon.
    *   Health decreased 100 -> **80**.
    *   Damage increased 166 -> **215**.
    *   Range increased 70 -> **75** (Matches Dox range).
    *   Rate of Fire decreased 0.61 -> 0.5.
*   **Stoke (Rework):** Now a dedicated Anti-Air platform.
    *   **Targeting:** Can ONLY target air units.
    *   Cost reduced to 180. Speed increased to 16. Damage increased to 40.
*   **Purger:** Cost increased to **60**. Damage decreased 450 -> 334. Added missile target tracking and increased mesh bounds.
*   **Maul:** Health decreased 1250 -> **1150**.
*   **Peacekeeper:** Health decreased 170 -> 130; Range decreased 70 -> 67.5; Vision increased 105 -> 115.
*   **Corsair:** Cost decreased from 300 to **200**. Speed decreased from 10 to **8**. Range decreased from 240 -> **160**. Damage increased 40 -> **60**. Rate of fire increased from 0.25 -> **0.3**. Ammo now **homes in** on targets in its final flight stage.
*   **Shank:** ~~Health decreased 300 -> 250; Damage decreased 125 -> 120. Removed Splash damage.~~
*   **Patriot:** Acceleration/Braking decreased 120 -> 30; Turn speed decreased 720 -> 360.
*   **Deathmark** Now prioritize Advanced Units and Structures. Cost decreased 1200 -> 1000; Now shoots a short burst of 2x 500
*   **Enforcer:** Range decreased 100 -> **95**; Move speed increased 12 -> **15**
*   **Monstrosity:**  Now prioritize Advanced Units and Structures. Speed increased 12 -> 15 Range decreased 170 -> 140 Vision range set to 150
---

## ✈️ Air Units
*   **Nova (Major Rework):** 
    *   HP increased 90 -> 150. 
    *   Function: Spawns a targetable "missile" suicide unit once triggered that chases enemies. 
    *   Targeting: No longer prioritizes bombers/transports over fighters.
*   **Lockheed (Rework):** 
    *   **Gun weapon has been removed.** 
    *   Reworked Missile Weapon: 2 weapons, 4 missiles each, 50 damage/splash per missile. Features a spread-fire pattern and a 10s reload between volleys.
*   **Marauder:** 
    *   Updated SI Icon. HP decreased 50 -> 40. Speed decreased 100 -> 90. 
    *   Weapon: Now fires 6 shots at max RoF (2/s), then RoF drops to 1/s. 
    *   Logic: Added `"maintain_priority_target": false` to main json.
*   **Scythe:** 
    *   Metal cost increased to **220**. 
    *   Range increased 95 -> 105. Damage increased 29 -> 35. Rate of Fire increased 0.9 -> 1. 
    *   Turn rate decreased 300 -> 240. Fire angle decreased 105 -> 60 degrees.
*   **Meteor:** Health reduced 2000 -> 750. Drones are now uncontrollable, cannot target air, and have halved movement/turn speeds.
*   **Dauntless:** Bomb initial and max velocity decreased 35 -> 20.
*   **Comet:** No longer buildable by Fabricators. Now produced exclusively from the Advanced Flyer Foundry.
*   **Firebird:** Missile range decreased 180 -> 160; Rate of Fire decreased 0.33 -> 0.25.

---

## 🚀 Orbital & Endgame
*   **Viper:** Range reduced 200 -> 100. Damage increased 40 -> **50**.
*   **Loki:** Main cannon no longer targets Air or Underwater/Seafloor. Side gun splash radius reduced 20 -> 5.
*   **Starcannon:** Strat icon priority lowered. Updated description to reflect max units held.

---

## 🎨 Visuals & Bugfixes
*   **New Models:** Fabrication Walker, Armour Fabricator, Guardian, Corsair, Panzer, Stoke, Radar, Deathmark, Scorpion, Shank, Dauntless, Flyer Fabricator, Scythe, Havoc, Osprey, Foundries, and more.
*   **Icon Updates:** New SI icons for Corsair, Marauder, and Nova.
*   **Bugfixes:** 
    *   Sea Urchin: Added missing unit type.
    *   Fabricators: Regular fabricators can no longer build Spoilers.