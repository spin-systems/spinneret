# Spinneret: `rainbowstream` Account Management

[github.com/spin-systems/spinneret](https://github.com/spin-systems/spinneret)

Multiple Twitter accounts with oauth token stored per account (shared `config.json`).

- The `spinner` command will take the name of a folder (corresponding to an authenticated Twitter account).
  - Script enters account folder and runs `rainbowstream` after backing up the oauth, and copying the token if one exists
  - Accounts in use are stored in a table `~/.rain_spinnerets.md`, marked with `[x]` when switched to (else `[ ]`)
- track which account was last using the tokens with `~/.rainbow_user` (added by this procedure, ensuring never left hanging if the system exits uncaught)
- `~/.scripts` (GitHub: `lmmx/dot-scripts`) contains a script at `rainstream/spinner` exporting a script at `exports/rainspinner` which switches these user files
  - supplying arguments to `spinner` could send tweets with the t command(?)
