# Az-Framework 2.0 txAdmin Recipe

This recipe deploys an Az-Framework 2.0 FiveM base with the core framework, merged framework modules, bridge-ready inventory settings, AMenu compatibility, and the current public Az resource pack.

## Files

- `azure-framework.yaml`: txAdmin recipe.
- `server.cfg`: the matching runtime config written by the recipe.
- `VALIDATION.txt`: recipe validation result.

## Installs

- CFX default resources without default chat.
- `oxmysql`, `ox_lib`, `ox_target`, `ox_inventory`, and `fivem-appearance` v1.3.1.
- `MugShotBase64`, `glitch-minigames`, `pma-voice`, `AMenu`, and `AMenu-Bridge`.
- `Az-Framework` with merged chat, banking, character UI, DMV, fuel, ID, daily rewards, death, insurance, housing, and Mors delivery modules.
- Az bridge repos for `qb-core`, `qb-inventory`, `qb-target`, `es_extended`, and `ND_Core`.
- Summer 2.0 resources including legal seasonal jobs, illegal seasonal contracts, and `Az-Summer2Core`.
- Public standalone Az resources that remain outside the framework core.
- `fivem-appearance` is installed from the v1.3.1 tag so the Az character creator can open full first-character appearance customization.

## Merged Resources

Do not install the old standalone `AChat`, `Az-Banking`, `Az-CharacterUI`, `Az-Dailyrewards`, `Az-Death`, `Az-DMV`, `Az-Fuel`, `Az-Id`, or `Az-MoresDelivery` repos with this recipe. Their runtime now comes from `Az-Framework`.

## Install

1. Host `azure-framework.yaml` from the `Azure-Framework/txRecipe` repository or paste the raw recipe URL into txAdmin.
2. Start a fresh txAdmin deployment.
3. Enter the server name, license key, and database details.
4. Run the recipe.
5. Add Discord bot/webhook values, local assets, maps, vehicles, weapons, and private admin identifiers after deployment.

## Database Compatibility

The recipe uses txAdmin's `connect_database` and `query_database` actions, then writes the generated `{{dbConnectionString}}` into `server.cfg` for `oxmysql`.

Supported database targets are the same style txAdmin and `oxmysql` expect:

- Local or remote MariaDB.
- Local or remote MySQL.
- Hosted databases from txAdmin-compatible FiveM hosts.

For best compatibility, keep the database name to letters, numbers, and underscores only. The recipe name is intentionally `Az Framework 20` so txAdmin generates a safe default database name such as `AzFramework20_168A81` instead of a name with punctuation.

Avoid database names like `Az-Framework2.0_168A81`; some MariaDB/MySQL parser paths treat the dot as a database/table separator during the txAdmin `connect_database` step.

## Security

The recipe does not contain live Cfx license keys, database credentials, Discord bot tokens, webhooks, or personal admin identifiers.
