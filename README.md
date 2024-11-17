# NewSuper Project

Welcome to the NewSuper project! This repository contains tools and functionalities for managing whitelists and max buy limits for our launchpad.

## Getting Involved

If you have any suggestions or issues, please create an issue [here](https://github.com/parzivalishan/newsuper/issues) or contact me directly on Telegram: [t.me/crypticishan](https://t.me/crypticishan).

---

## Whitelist Functionality

The whitelist function can be disabled by adding the dead address `0x000000000000000000000000000000000000dead` to the `whitelist.json` file. It may take a few minutes for changes to reflect in the frontend of the Launchpad.

### Example `whitelist.json`:

```json
{
    "whitelistedAddresses": [
        "0x000000000000000000000000000000000000dead",
        "0x29de0cc374FC3432A9D9dE753BF12995E138DFf9",
        "0xE996BbDE2B2674bA8B4b3aae0E5C0E17e5B11dB9",
        "0x1736d80Db5da96ebA538Fb7CB90BF9d3eb0e0480"
    ]
}
```

- Setting the whitelist function to `false` allows all wallets to access the launchpad.
- If you modify the dead address (e.g., changing `0x000000000000000000000000000000000000dead` to `0x000000000000000000000000000000000000dea`), the whitelist function will revert to `true`, restricting access to only those wallets listed in the JSON.

---

## Max Buy Limit Functionality

The `maxBuyLimit` function sets a maximum purchase limit for each wallet address. 

### Example `maxBuyLimits.json`:

```json
{
    "maxBuyLimits": {
        "0x000000000000000000000000000000000000dead": 300,
        "0xad3a5DdCe484251f8839f185896b14605b8dd340": 5,
        "0x29de0cc374FC3432A9D9dE753BF12995E138DFf9": 100,
        "0xE996BbDE2B2674bA8B4b3aae0E5C0E17e5B11dB9": 10
    }
}
```

- The dead address will override any other address limits, meaning it will always have a maximum buy limit of 300, regardless of other settings.

---

