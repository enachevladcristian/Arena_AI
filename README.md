# The Sphere

An idle defense game: your sphere automatically fires at approaching enemies while you invest cash in upgrades. Each completed wave awards Wave Coins. After losing, spend them in the permanent shop on starting damage, health, and cash earnings. Survive to wave 10 to unlock rebirth and earn permanent damage bonuses from Sphere Shards. Coins and permanent upgrades persist through both losses and rebirths.

## Run locally

```sh
npm install
npm run dev
```

Open the local URL printed by Vite. Progress is saved automatically in your browser's local storage. Battles run while the page is open; offline progress is not simulated.

Use the pause and speed controls above the arena, and switch between Attack, Defense, and Utility to see all upgrades. The question mark in the top bar opens the field guide.

## Levels and skins

Completed waves also count toward a permanent level: level 1 takes 3 waves, level 2 takes 6, level 3 takes 12, and each later level takes twice as many waves as the previous one. The first three level completions unlock skins. Equip one skin at a time to increase all stats by 5%; skins do not stack. Level progress and equipped skins persist after a loss or rebirth.

## Combat and economy

Every seventh wave includes a boss with six times a normal enemy's health, three times its impact damage, and a larger cash reward. Critical chance starts at 0% and increases by 1 percentage point per upgrade up to 45%. Critical damage is the total damage of a critical shot: it starts at 100% of normal damage and increases by 2 percentage points per upgrade up to 150%. A skin's 5% combat-stat bonus applies to critical stats without exceeding their caps.

Each armor upgrade adds 5 armor. Damage taken is multiplied by `100 / (100 + armor)`. The Kill Bonus begins at 2 cash per five enemies defeated and rises by 5 per upgrade. Wave Coins begin at 5 per completed wave and rise by 10 per upgrade; they are used in the permanent shop. These two utility upgrades are run upgrades and reset after a loss or rebirth. Skin bonuses do not alter the fixed kill and wave payouts.

Use the theme selector in the top bar to switch between purple, green, and red. Your selection is stored in the browser and doesn't change gameplay or equipped skins.
