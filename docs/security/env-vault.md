---
layout: docs
title: ".env.vault Identifier - Security"
redirect_from:
  - /env-vault
---

##### Security

# .env.vault Identifier

The .env.vault file uniquely identifies your project in dotenv-vault. You SHOULD commit this file to source control. It is safe to do so. Aside: DON'T commit your [.env](/docs/security/env) or [.env.me](/docs/security/env-me) to source control.

You can think of it like a unique git url at GitHub. It identifies your project so that your teammates pull the correct .env file from dotenv-vault.

#### Example

Here's an example of what a .env.vault file looks like:

```
DOTENV_VAULT=vlt_9a165d…
```

The first thing you might notice is the formatting is the same as a .env file. This is intentional to allow for maximum future interoperability.

The DOTENV_VAULT key is important. It is required. It is that value that identifies your project uniquely to the dotenv vaulting mechanisms.

#### Generating

You can generate a .env.vault file at [ui.dotenv.org](https://ui.dotenv.org/ui1/project/new) or through [dotenv-vault](https://github.com/dotenv-org/dotenv-vault). The process is similar to creating and cloning your very first git repo on GitHub.
