# Pattern Arcade — Get Funded

A roguelike paper-trading arcade game in a single HTML file. Trade a synthetic
random-walk market (long/short, leverage, liquidations) and hit each level's
profit target within 3 trading days — inspired by the run structure of Balatro
and Clover Pit.

**Everything is simulated. No real market data, no real money, not investment
advice.**

## How to play

Open `index.html` in a browser (or serve the folder with any static file
server). No build step, no dependencies.

- **Levels**: reach the profit target (+25% on level 1, +35% after) within
  3 trading days (180 ticks). Miss it and the run resets.
- **Trading**: long/short with 25/50/100% position size. Leverage starts
  capped at 2x — 5x unlocks at level 3, 10x at level 5. A losing position
  that eats its full margin is liquidated.
- **Relics**: clearing a level offers a pick of 1 from 3 passive upgrades
  (14 in the pool), with synergies — streak stacking, hold-time bonuses,
  liquidation insurance, contrarian payouts, a coin-flip gamble.
- **Boss levels**: every 3rd level draws a market modifier — hidden regime
  tag, faster regime flips, trade fees, earlier liquidation, higher target,
  or a shortened 2-day session.
- **Missions**: each level has an optional side objective worth +10% cash,
  paid out before the target check — a finished mission can rescue a
  near-missed level.
- **Meta progression**: busted runs pay out Insight, spent on permanent
  upgrades (starting cash, easier level 1) that persist across runs via
  localStorage.

## Notes

The market is a seeded random walk with a per-level regime plan that always
contains at least one real uptrend and one real downtrend segment, so the
target is always reachable by reading the chart — never gated on RNG luck.
