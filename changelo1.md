# Sunrise — Unit Diff vs. Legion Expansion

## Air

**Nova**
- `build_metal_cost` increased from 180 to 200
- `max_health` decreased from 180 to 150
- `guard_radius` increased from 0 to 160
- `spawn_unit_on_death_with_velocity` changed from false to true
- `max_range` increased from 10 to 50 (main and deploy weapons)
- `no_busy_auto_attack` changed from true to false

**AOE Nova** (triggered bomb)
- `max_health` decreased from 500 to 220
- `navigation`/`move_speed` increased from 0 to 130
- `guard_radius` added, set to 160
- `nearby_target_tick_update_interval` added, set to 1
- `wreckage_health_frac` added, set to 0.0
- `max_range` decreased from 80 to 5
- `yaw_range` increased from 0 to 360
- `pitch_range` increased from 0 to 360
- `self_destruct` added, set to true
- `target_priorities` added: `Mobile & Air`
- Ammo `damage` decreased from 6 to 0
- Ammo `splash_damage` decreased from 6 to 0
- Ammo `splash_radius` decreased from 80 to 0
- Ammo `full_splash_damage_radius` decreased from 80 to 0
- Death `damage` increased from 35 to 150
- Death `splash_damage` added, set to 150
- Death `splash_radius` decreased from 70 to 15
- Death `full_splash_damage_radius` increased from 0 to 5
- Death `damage_volume`/`initial_radius` increased from 5.0 to 20.0
- Death `damage_volume`/`delay` decreased from 1 to 0.01
- Death weapon `ammo_capacity` and `ammo_per_shot` decreased from 20 to 15

**Meteor**
- `max_health` decreased from 2000 to 750
- `navigation`/`aggressive_behavior` added, set to `circle`
- `navigation`/`aggressive_distance` added, set to 230
- `navigation`/`circle_min_time` added, set to 10.0
- `navigation`/`circle_max_time` added, set to 20.0
- `navigation`/`bank_factor` added, set to 2

**Meteoroid** (Meteor drone)
- `navigation`/`move_speed` decreased from 80 to 40
- `navigation`/`turn_speed` decreased from 240 to 120
- `target_layers` removed `WL_Air`

**Scythe**
- `build_metal_cost` decreased from 240 to 200
- `navigation`/`turn_speed` decreased from 300 to 240
- Ammo `damage` increased from 29 to 35
- `base_spec` changed from `base_shell_turret` to `base_fighter_turret`
- `max_range` decreased from 110 to 107.5
- `firing_arc_yaw` decreased from 70 to 60
- `yaw_range` decreased from 70 to 0
- `pitch_rate` increased from 360 to 3600

**Dauntless**
- `navigation`/`move_speed` increased from 75 to 80
- `navigation`/`acceleration` increased from 75 to 80
- `navigation`/`brake` increased from 20 to 25
- Ammo `initial_velocity` and `max_velocity` decreased from 40.0 to 25.0
- Ammo `full_damage_splash_radius` decreased from 2 to 1
- `ammo_capacity` decreased from 425 to 424

**Firebird**
- Rocket `max_range` decreased from 180 to 160
- Rocket `rate_of_fire` decreased from 0.33 to 0.25
- `projectiles_per_fire` added, set to 1 per gun
- Rocket muzzles reduced from 4 to 2

**Lockheed**
- `maintain_priority_target` added, set to false
- Rockets moved to the primary tool slot, gun to secondary
- Gun `max_range` decreased from 80 to 60
- Gun `rate_of_fire` decreased from 4 to 2
- Rocket `damage` decreased from 250 to 85
- Rocket `splash_damage` added, set to 85
- Rocket `splash_radius` added, set to 5
- Rocket `full_damage_splash_radius` increased from 2 to 3
- Rocket `turn_rate` added, set to 0
- Rocket `ammo_capacity` increased from 5 to 10
- Rocket `ammo_per_shot` increased from 2.5 to 3
- Rocket `rate_of_fire` increased from 2.5 to 5
- Rocket `max_range` decreased from 100 to 60
- Rocket `firing_standard_deviation` decreased from 30 to 5
- Rocket `firing_arc_yaw` and `firing_arc_pitch` decreased from 180 to 0
- Rocket `yaw_range` and `pitch_range` increased from 0 to 180

**Marauder**
- `max_health` decreased from 50 to 40
- `navigation`/`move_speed` decreased from 100 to 90
- `maintain_priority_target` added, set to false
- `ammo_capacity` added, set to 6
- `ammo_per_shot` added, set to 1
- `ammo_demand` added, set to 1
- `ammo_source` added, set to `time`
- `target_priorities` added: `Fabber`, `AirDefense`, `Mobile & (Land | Naval)`

**Osprey**
- `build_metal_cost` increased from 100 to 165
- `max_health` decreased from 55 to 50
- `navigation`/`move_speed` decreased from 100 to 85
- `navigation`/`brake` increased from 40 to 80
- `recon`/`observer` radius increased from 70 to 120
- `transporter`/`load_range` added, set to 15
- `unit_types` added `UNITTYPE_Offense`

**Comet**
- `unit_types` changed `UNITTYPE_FabAdvBuild` to `UNITTYPE_FactoryBuild`
- `command_caps` removed `ORDER_SpecialMove`
- `wreckage_health_frac` added, set to 0.5

**Infiltrator**
- `unit_types` added `UNITTYPE_Offense`

**Fabrication Flyer**
- `max_health` decreased from 165 to 85

**Salamander**
- `base_spec` moved to the rebuilt `l_bomber_heavy` chassis
- `navigation`/`move_speed` increased from 40 to 60

**Purifier** (Salamander drop turret)
- `base_spec` moved to the rebuilt `l_bomber_heavy` chassis
- `mesh_bounds` decreased from 10/10/8 to 3.5/3.5/5
- `command_caps` added `ORDER_FireSecondaryWeapon`
- Muzzles reduced from 2 to 1

**Loki**
- All four tools changed to a single new `tripod_tool_weapon`
- `damage` decreased from 800 to 100
- `splash_damage` decreased from 300 to 50
- `splash_radius` decreased from 40 to 3
- `full_damage_splash_radius` decreased from 5 to 1
- `max_range` decreased from 150 to 140
- `rate_of_fire` increased from 0.5 to 10
- `ammo_capacity` added, set to 10.1
- `ammo_per_shot` added, set to 0.2
- `ammo_demand` added, set to 1
- `ammo_source` added, set to `time`
- `carpet_fire` and `carpet_wait_for_full_ammo` added, set to true
- `spread_fire` changed from false to true
- `pitch_range` decreased from 60 to 45
- `pitch_rate` increased from 20 to 180
- `yaw_rate` increased from 40 to 45
- `idle_aim_delay` increased from 2 to 5
- `initial_velocity` and `max_velocity` set to 700.0
- `target_layers` removed `WL_Air` and `WL_Underwater`
- Side gun `splash_radius` decreased from 25 to 5
- Side gun `full_damage_splash_radius` decreased from 20 to 5

---

## Land

**Predator** (new)
- `build_metal_cost` 100
- `max_health` 100
- `navigation`/`move_speed` 15, `acceleration` and `brake` 150, `turn_speed` 180
- `recon`/`observer` radius 130
- `unit_types` includes `UNITTYPE_CannonBuildable`

**Lancer**
- `build_metal_cost` decreased from 150 to 125
- `max_health` decreased from 100 to 70
- Ammo `damage` increased from 166 to 225
- `max_range` increased from 70 to 80
- `rate_of_fire` decreased from 0.61 to 0.4

**Peacekeeper**
- `max_health` decreased from 170 to 60
- `shield` added: `max_health` 35, `radius` 1, `energy_demand` 15, `recharge_rate` 2.5, `cooldown_time` 10, `recharge_requires_efficiency` true
- `energy_efficiency_requirement` added, set to 0.9
- `navigation`/`type` changed from `amphibious` to `land-small`
- `recon`/`observer` radius increased from 105 to 115
- `max_range` decreased from 70 to 67.5
- `unit_types` added `UNITTYPE_Shield`

**Stoke**
- `build_metal_cost` decreased from 210 to 170
- `navigation`/`move_speed` increased from 14 to 16
- Ammo `damage` increased from 39 to 50
- `max_range` increased from 80 to 100
- `pitch_rate` increased from 120 to 360
- `yaw_rate` increased from 160 to 360
- `target_layers` changed from `WL_LandHorizontal`/`WL_Seafloor`/`WL_WaterSurface` to `WL_Air`
- `target_priorities` added: `Air & ( EnergyProduction | Transport | Bomber | Gunship | Titan )`, `Mobile & Air`
- Ammo `flight_type` added, set to `Staged` (3 stages, `cruise_height` 20)
- Ammo `initial_velocity` and `max_velocity` increased from 200.0 to 250.0
- Ammo `lifetime` increased from 1 to 15
- Ammo `turn_rate` added, set to 30
- Ammo `physics`/`ignore_gravity` added, set to true

**Patriot**
- `navigation`/`acceleration` and `brake` decreased from 120 to 30
- `navigation`/`turn_speed` decreased from 720 to 360
- `projectiles_per_fire` added, set to 4
- Ammo `base_spec` changed from `base_missile_aa_seeking` to `base_laser_blast`
- Ammo `damage` decreased from 25 to 7.5
- Ammo `splash_damage` added, set to 7.5
- Ammo `splash_radius` added, set to 1
- Ammo `initial_velocity` and `max_velocity` increased from 200.0 to 280
- Ammo `lifetime` decreased from 1.0 to 0.5
- Ammo `turn_rate` removed (was 3600.0)
- `firing_standard_deviation` added, set to 3
- `firing_move_speed_multiplier` added, set to 0.5
- `targeting_move_speed_multiplier` added, set to 0.5
- `targeting_disable_pushing` added, set to true

**Orbweaver**
- `max_health` increased from 400 to 480

**Enforcer**
- `navigation`/`move_speed` increased from 12 to 15
- `max_range` decreased from 100 to 95

**Maul**
- `build_metal_cost` decreased from 300 to 170
- `max_health` decreased from 1150 to 600
- `rate_of_fire` decreased from 1 to 0.5

**Shank**
- Ammo `damage` increased from 125 to 130
- Ammo `splash_damage` increased from 20 to 60
- Ammo `splash_radius` decreased from 5 to 3
- Ammo `physics`/`type` added, set to `Projectile`
- Ammo `physics`/`gravity_scalar` added, set to 5
- Ammo `physics`/`allow_underground` added, set to true

**Corsair**
- `build_metal_cost` decreased from 300 to 220
- `max_health` decreased from 175 to 100
- `rate_of_fire` increased from 0.25 to 0.3
- `default_firing_pitch` added, set to -65
- Ammo `flight_type` added, set to `Staged` (3 stages, `cruise_height` 60)
- Ammo `initial_velocity` decreased from 200 to 120
- Ammo `max_velocity` decreased from 400 to 50
- Ammo `physics`/`gravity_scalar` increased from 6 to 10
- Ammo `splash_damage` decreased from 40 to 30
- Ammo `splash_radius` decreased from 10 to 8
- `target_priorities` added: `Structure & SurfaceDefense`, `Structure & Defense`, `Commander`

**Panzer**
- `target_layers` changed from `WL_LandHorizontal`/`WL_WaterSurface`/`WL_Orbital` to `WL_Air`/`WL_Orbital`
- `target_priorities` added: `Structure & SurfaceDefense`, `Structure & Defense`, `Commander`, `Mobile - Air`, `Structure - Wall`, `Wall`

**Miniman**
- `ammo_capacity` increased from 7 to 8
- Bomb `armor_damage_map`/`AT_Structure` decreased from 3.0 to 1.0

**Purger**
- `build_metal_cost` increased from 50 to 60
- `attack_range_frac` added, set to 0.8
- `maintain_priority_target` added, set to false
- `mesh_bounds` increased from 3.5/3/2.8 to 3.75/3.5/5
- Ammo `base_spec` changed from `base_artillery` to `base_missile_aa_seeking`
- Ammo `damage` decreased from 450 to 334
- Ammo `initial_velocity` increased from 80 to 150
- Ammo `lifetime` decreased from 30 to 1
- Ammo `turn_rate` added, set to 60.0
- Ammo `armor_damage_map`/`AT_Structure` added, set to 1.0
- `ammo_capacity` added, set to 1
- `ammo_per_shot` added, set to 1
- `ammo_demand` added, set to 10
- `ammo_source` added, set to `energy`
- Jump tool `auto_attack` changed from false to true
- `no_busy_auto_attack` changed from true to false

**Monstrosity**
- `navigation`/`move_speed` increased from 12 to 15
- `navigation`/`acceleration` increased from 10 to 15
- `recon`/`observer` radius increased from 100 to 150
- `max_range` decreased from 170 to 140
- `target_priorities` added: `Advanced - Structure`, `Tank - Structure`, `Mobile - Air`, `Structure - Wall`, `Wall`

**Deathmark**
- `build_metal_cost` decreased from 1200 to 1000
- `maintain_priority_target` added, set to false
- Ammo `damage` decreased from 1000 to 500
- Ammo `initial_velocity` decreased from 200 to 100
- Ammo `max_velocity` decreased from 500 to 300
- Ammo `physics`/`gravity_scalar` decreased from 26 to 20
- `rate_of_fire` increased from 0.142 to 10
- `ammo_capacity` added, set to 7
- `ammo_per_shot` added, set to 7
- `ammo_demand` added, set to 1
- `ammo_source` added, set to `time`
- `carpet_fire` and `carpet_wait_for_full_ammo` added, set to true
- `target_priorities` added: `Advanced - Structure`, `Tank - Structure`, `Mobile - Air`, `Structure - Wall`, `Wall`

**Havoc**
- Ammo `damage` decreased from 750 to 500
- `ammo_chain_damage` added, set to 500.0
- `ammo_chain_jumps` added, set to 2
- `ammo_chain_range` added, set to 50.0
- `ammo_chain_damage_falloff` added, set to 1
- `ammo_chain_travel` added, set to true
- Ammo `initial_velocity` decreased from 200.0 to 100.0
- Ammo `max_velocity` decreased from 300.0 to 150.0
- `spawn_unit_on_death` removed (mine chain)
- Second tool (missile intercept beam) removed

**Earthshaker**
- `build_metal_cost` decreased from 1800 to 1400
- `max_health` decreased from 7000 to 2000
- `navigation`/`turn_speed` decreased from 180 to 60
- Weapon tool removed
- `shield` added: `max_health` 5000, `radius` 75, `energy_demand` 2000, `recharge_rate` 300, `cooldown_time` 10, `recharge_requires_efficiency` true
- `energy_efficiency_requirement` added, set to 0.9
- `unit_types` added `UNITTYPE_Shield`

**Scorpion**
- `build_metal_cost` increased from 900 to 1100
- `max_health` increased from 1650 to 2000
- Ammo `damage` increased from 500 to 750
- Ammo `splash_damage` increased from 150 to 250
- Ammo `splash_radius` decreased from 15 to 5
- `rate_of_fire` increased from 0.4 to 0.6

**Necromancer**
- `projectiles_per_fire` increased from 7 to 14
- `ammo_capacity` and `ammo_per_shot` increased from 420 to 750
- `ammo_demand` increased from 35 to 45
- `transportable`/`size` added, set to 1

**Investigator**
- `build_metal_cost` decreased from 150 to 100
- `recon`/`observer` radius increased from 150 to 200
- Radar mode `recon`/`observer` radius increased from 0 to 75
- Radar mode `consumption`/`energy` increased from 100 to 200

---

## Structures

**Jackal**
- `build_metal_cost` decreased from 325 to 275
- `max_health` increased from 750 to 1000

**Scarab**
- `build_metal_cost` decreased from 550 to 450
- `max_health` increased from 2500 to 3000
- `max_range` increased from 110 to 120
- `mesh_bounds` decreased from 17.06/17.06/16.78 to 13.4/17.41/10.89

**Rampart**
- `max_health` increased from 750 to 1500
- `shield` added: `max_health` 15000, `radius` 100, `energy_demand` 6000, `recharge_rate` 200, `cooldown_time` 30, `recharge_requires_efficiency` true
- `ammo_capacity` increased from 36000 to 60000
- `ammo_demand` increased from 1000 to 1200
- `mesh_bounds` decreased from 30/30/27 to 15/15/13.5
- `placement_size` decreased from 30/30 to 15/15
- `wreckage_health_frac` added, set to 0.4
- Long-range interceptor tool removed

**Shredder**
- `unit_types` added `UNITTYPE_CombatFabBuild`

**Radar**
- `max_health` increased from 500 to 750
- `recon`/`observer` radius increased from 100 to 200
- `mesh_bounds` decreased from 13.85 to 6.694

**Hive**
- `l_swarm_hive_reclaim_arm` tool added: `auto_reclaim` true, `auto_repair` false, `construction_demand`/`metal` 60, `max_range` 180
- Main weapon `auto_reclaim` added, set to true

**Reclaim Turret** (new)
- `auto_reclaim` true, `auto_repair` false
- `construction_demand`/`metal` 30, `construction_demand`/`energy` 400
- `max_range` 200
- `reclaim_types` limited to `Wreckage` and `Feature`

**Liberator** (new registration)
- Added to `unit_list.json` and `unit_list_legion.json` (spec unchanged from Legion)

**Barricade**
- `display_name` changed from Clot to Barricade
- `area_build_separation` increased from 1 to 1.2

**Power Catalyst**
- `production`/`energy` increased from 600 to 700
- `death_weapon` added, 500 damge over 20 radius with 2.5s delay

**Advanced Power Catalyst**
- `build_metal_cost` increased from 2500 to 2800
- `max_health` decreased from 2500 to 2000
- `production`/`energy` increased from 6000 to 9000
- `mesh_bounds` increased from 25/25 to 30/30

**OmniSilo Storage Device**
- `max_health` increased from 5000 to 7500
- `storage`/`energy` decreased from 225000 to 75000
- Death weapon `damage` and `splash_damage` decreased from 1200 to 500
- `mesh_bounds` decreased from 28/28/25 to 20/20/14.2

**Mass Extractor**
- `replaceable_units` removed `bug_advanced_extractor`

**Walker Foundry / Armour Foundry**
- `construction_demand`/`metal` decreased from 17 to 15
- `construction_demand`/`energy` decreased from 765 to 675

**Advanced Walker / Armour / Flyer Foundry**
- `construction_demand`/`metal` decreased from 50 to 45
- `construction_demand`/`energy` decreased from 1650 to 1500

**Advanced Ship Foundry**
- `construction_demand`/`metal` decreased from 65 to 60
- `construction_demand`/`energy` decreased from 1900 to 1750

---

## Fabricators

**Fabrication Walker**
- `max_health` decreased from 65 to 30
- `navigation`/`move_speed` increased from 14 to 15
- `shield` added: `max_health` 30, `radius` 1, `energy_demand` 30, `recharge_rate` 1.5, `cooldown_time` 10

**Advanced Fabrication Walker**
- `build_metal_cost` decreased from 2000 to 1900
- `max_health` increased from 150 to 400
- `navigation`/`move_speed` decreased from 14 to 10
- `construction_demand`/`energy` decreased from 2200 to 1900
- `has_death_effects` added, set to true

**Armour Fabricator**
- `build_metal_cost` increased from 200 to 250
- `max_health` increased from 185 to 200
- `navigation`/`move_speed` decreased from 11 to 10
- `construction_demand`/`metal` increased from 13 to 16
- `construction_demand`/`energy` increased from 850 to 1100

**Advanced Armour Fabricator**
- `max_health` decreased from 500 to 200
- `navigation`/`move_speed` increased from 10 to 16
- `construction_demand`/`metal` decreased from 70 to 60

**Guardian**
- `build_metal_cost` decreased from 350 to 250
- `construction_demand`/`metal` decreased from 45 to 30
- `construction_demand`/`energy` decreased from 600 to 400

---

## Sea

**Talos**
- AA ammo `base_spec` changed from `base_beam` to `base_laser_blast`
- AA ammo `damage` decreased from 20 to 10
- AA ammo `splash_damage` increased from 0 to 10
- AA ammo `splash_radius` increased from 0 to 1
- AA ammo `initial_velocity` and `max_velocity` added, set to 280
- AA ammo `lifetime` added, set to 0.7
- AA `base_spec` changed from `base_shell_turret` to `base_bot_weapon`
- AA `max_range` decreased from 180 to 110
- AA `rate_of_fire` increased from 1 to 2
- AA `yaw_range` increased from 180 to 360
- AA `pitch_range` decreased from 180 to 90
- AA `firing_standard_deviation` added, set to 3
- AA `idle_aim_delay` added, set to 0
- AA `spread_fire` added, set to true
- AA `target_layers` added `WL_AnySurface`

---

## Orbital

**Viper**
- Ammo `damage` increased from 40 to 50
- `max_range` decreased from 200 to 100
- `attack_range_frac` added, set to 0.75

**Paladin**
- `attack_range_frac` added, set to 0.9

**Starcannon**
- `factory`/`hide_stored_units` changed from true to false
- `factory`/`spawn_points` increased from 9 (8 shared) to 14 distinct bones
- Ammo `ground_target_area_spread` increased from 30 to 50
- `strategic_icon_priority` added, set to 4

**Starship Projector**
- `factory`/`spawn_points` changed from `bone_platform` to `socket_shell`

**Centurion**
- `wreckage_health_frac` added, set to 0.0

---

## Unit list

- Added `l_attack_vehicle` (Predator), `l_scout_turret` (Liberator) and `l_turret_reclaim` (Reclaim Turret)
- Removed `radar_jammer`, `tank_jammer`, `orbital_mine` and `tank_anti_nuke`
- Commander `l_base` `unit_types` added `UNITTYPE_Fabber`
- `l_tank_adv_support` is listed but has no spec files in the mod
- The `l_deffense_satelite` folder is shipped but unreferenced; the live Centurion still uses Legion's tool and ammo specs
