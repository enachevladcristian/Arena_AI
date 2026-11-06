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

Completed waves also count toward a permanent level: level 1 takes 3 waves, level 2 takes 6, level 3 takes 12, and each later level takes twice as many waves as the previous one. Each level completion unlocks a skin. Skin bonuses grow by 5 percentage points each time: +5%, +10%, +15%, and so on. Only the five most recent unlocked skins are available, and only one can be equipped at a time. When an equipped skin rotates out, the newest skin is equipped automatically. Previously unlocked skins that rotate out can still be viewed in the Archive tab, but cannot be equipped. Level progress and equipped skins persist after a loss or rebirth.

## Combat and economy

Every seventh wave includes a boss with six times a normal enemy's health, three times its impact damage, and a larger cash reward. Critical chance starts at 0% and increases by 1 percentage point per upgrade up to 45%. Critical damage is the total damage of a critical shot: it starts at 100% of normal damage and increases by 2 percentage points per upgrade up to 150%. A skin's combat-stat bonus applies to critical stats without exceeding their caps.

Each armor upgrade adds 5 armor. Damage taken is multiplied by `100 / (100 + armor)`. The Kill Bonus begins at 2 cash per five enemies defeated and rises by 5 per upgrade. Wave Coins begin at 5 per completed wave and rise by 10 per upgrade; they are used in the permanent shop. These two utility upgrades are run upgrades and reset after a loss or rebirth. Skin bonuses do not alter the fixed kill and wave payouts.

Use the theme selector in the top bar to switch between purple, green, and red. Your selection is stored in the browser and doesn't change gameplay or equipped skins.

## Auto Battle

Enable Auto Battle below the arena to start a fresh run five seconds after defeat. Run cash and upgrades reset as usual, while coins, shards, permanent upgrades, level progress, and skins are retained. Cancel the countdown or open the permanent shop to turn Auto Battle off; opening the shop never spends coins automatically. The setting is saved in the browser. Progress (including the countdown) advances only while the game page is running.

## Battle speed

The speed button above the arena cycles between 1× and 2×. Purchase the 3× speed unlock in Utility for 500 run cash to add 3× to the cycle. This one-time unlock persists through losses, rebirths, and browser reloads; it does not change the Auto Battle countdown.

Attack range starts at 210 m and increases by 7 m per upgrade, up to 15 upgrades (315 m before skin bonuses). Existing saves with more than 15 range upgrades are capped at level 15.
