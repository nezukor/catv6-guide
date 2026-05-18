\# Useful Globals



These variables and functions are available globally in `main.luau`:



\### Player \& Entity

\- `entitylib.isAlive` — boolean (is local player alive)

\- `entitylib.character` — local player entity table

\- `entitylib.character.RootPart` — HumanoidRootPart

\- `entitylib.character.Humanoid` — Humanoid

\- `entitylib.List` — table of all targetable entities

\- `lplr` — LocalPlayer



\### Game State

\- `store` — shared game state

\- `store.KillauraTarget` — current killaura target

\- `store.inventory.inventory.items` — local player’s items



\### Utilities

\- `notif('Title', 'Message', duration, 'info'|'alert')`

\- `gameCamera` — workspace.CurrentCamera

\- `runService` — RunService (cloneref'd)



\### Bedwars Specific

\- `bedwars.KnockbackUtil.applyKnockback`

\- `bedwars.SwordController`

\- `bedwars.ItemMeta\[itemType]`

\- `bedwars.Client:Get(remoteName)`

\- `remotes.AttackEntity`

\- `remotes.FireProjectile`

