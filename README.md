IncPop v1.0.0 — Incursion Coffer Popper
Author: Soliserio

A standalone Windower addon for opening all fourteen normal and grand Incursion coffer types.

Opening order:
Velkk → Ymmr-Ulvid → Ignor-Mnt → Durs-Vike → Tryl-Wuj → Liij-Vok → Gramk-Droog.

Opens normal coffers before grand coffers within each group and skips types you do not have.

Features:
- Current-character and all-local-character commands.
- Inventory-only operation; no storage transfers.
- Requires at least 10 free Inventory slots before each use.
- Confirms consumption through inventory count changes.
- Stops on unconfirmed use or unexpected inventory changes without automatically retrying.
- Cancellation and status commands.
- Stops when engaging, resting, dying, zoning or logging out.
- Does not open unrelated containers.

Installation:
Extract the ZIP and place the incpop folder inside Windower/addons.

Commands:
//lua load incpop
//incpop start
//incpop start all
//incpop cancel
//incpop cancel all
//incpop status

For all-character operation, load IncPop on every local client first. With the Send addon:
//send @all //lua load incpop

Stand still, disengaged, with menus closed. Do not manually move or use coffers while running. Cancellation cannot undo an item use already sent. Consumption confirmation does not verify every reward.

Testing:
Fourteen offline tests passed. Single-coffer and all-character operation were confirmed in game by the author.

The ZIP includes the addon and installation/usage instructions.
