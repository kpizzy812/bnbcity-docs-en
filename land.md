# Land

## Overview

Land is a separate asset in BNB City. Before building, you must own a plot. Plots can be bought from the mayor (primary sale) or from other players (P2P market).

## Land Types

| Plot | Physical Size | Price | Available Tiers |
|------|--------------|-------|-----------------|
| Mini 1x1 | 1 cell | 0.002 BNB | T0, T1, T2 |
| Standard 1x1 | 1 cell | 0.008 BNB | T3, T4 |
| Large 2x2 | 4 cells | 0.045 BNB | T5, T6 |
| Mega 3x3 | 9 cells | 0.125 BNB | T7 |

## Primary Sale (From the Mayor)

The city mayor sells plots as the city grows:
- Plots open in rings from center to outskirts
- Fixed price per land type
- 100% of land sale revenue goes to the mayor (admin)
- No limit on plots per wallet
- Empty land has no tax or timer -- it just sits there

**Location matters:** Central plots (first rings) are the most prestigious. Early players get the best spots.

## Land Upgrade

You can upgrade a **Mini 1x1** plot to a **Standard 1x1** plot for **0.006 BNB** (the price difference). This lets you start small with a T0--T2 building and later upgrade the land to support T3--T4 buildings, without buying a new plot.

The upgrade preserves your plot location -- you keep the same coordinates.

## Roads

Roads are the city's infrastructure, built only by the mayor:
- You can only buy land **adjacent to a road**
- Roads control the pace of city expansion
- Roads have no economic logic (no cost, no yield)
- Stored off-chain (not in the smart contract)

## Empty Land

A plot without a building:
- Generates no income
- Has no maintenance cost
- Can be sold on the P2P market
- Can be built on at any time

## Plot with a Completed Building

When a building finishes its cycle:
- Demolish the building (free) to free the plot
- Build a new business on the same plot
- Or sell the empty plot on the marketplace
