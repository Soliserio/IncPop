# IncPop

A Windower addon that opens Incursion coffers from Inventory, one at a time, with consumption checks and room reserved for rewards.

**Version: 1.0.0**

## Supported Coffers

Regular and Grand variants for:

- Velkk
- Ymmr
- Ignor
- Durs
- Tryl
- Liij
- Gramk-Droog

## Installation

1. Place the `incpop` folder inside `Windower/addons/`.
2. Load the addon using the command below.

`//lua load incpop`

Loading the addon does not open any coffers.

## Before Starting

- Be alive, idle, and disengaged.
- Place the coffers you want opened in Inventory.
- Keep at least 10 free Inventory slots for rewards.
- Avoid manually using or moving coffers while IncPop is running.

IncPop does not retrieve coffers from other bags.

## Single-Character Commands

### Test one coffer

`//incpop test`

Opens one supported coffer and stops after confirming consumption.

### Open available coffers

`//incpop start`

Opens supported coffers in Inventory until none remain or a stop condition occurs.

### Cancel

`//incpop cancel`

Stops further queued uses. An item action already sent may still finish.

### Check status

`//incpop status`

Shows whether IncPop is idle or running, including the number of confirmed uses during the current run.

## All-Client Commands

IncPop must be loaded on every participating local client. These commands use the addon's built-in local-client messaging.

### Test one coffer per client

`//incpop test all`

### Start on all loaded clients

`//incpop start all`

### Cancel on all loaded clients

`//incpop cancel all`

These commands affect local clients running IncPop, not other players.

## Timing and Confirmation

IncPop waits one second before starting. After confirming that a coffer count decreased by exactly one, it waits three seconds before continuing.

If consumption is not confirmed within 15 seconds, it stops without automatically retrying.

## Stop Conditions

IncPop stops when:

- Fewer than 10 Inventory slots are free before the next use.
- The character becomes engaged, rests, dies, or becomes unavailable.
- Inventory cannot be read.
- A coffer count changes unexpectedly.
- Consumption cannot be confirmed.
- The character zones or logs out.
- You cancel the request.

When no supported coffers remain in Inventory, IncPop reports completion.

## Updating

Replace `incpop.lua`, then reload while no opening sequence is active:

`//lua reload incpop`

**Author: Soliserio**
