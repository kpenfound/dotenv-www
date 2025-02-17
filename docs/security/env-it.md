---
layout: docs
title: "Integration Tokens - Security"
redirect_from:
  - /env-it
---

##### Security

# Integration Tokens

Integration tokens, also known as IT tokens, are limited access tokens.

While a .env.me credential permits [push](/docs/dotenv-vault/push) and [pull](/docs/dotenv-vault/pull) across ALL environments, an IT token does not. IT tokens can ONLY pull and only for a single environment.

This means you cannot create an IT token to pull both staging secrets and production secrets. You instead have to generate two separate IT tokens - one for production and one for staging. This is by design to further protect your secrets and practice the principle of least privilege.

How can I get an IT token? They are auto-generated for you when you add an integration to an environment.

#### Example

Here's an example of what an IT Token looks like:

```
it_e3811a4…
```

Here's an example of it put to use:

```
$ npx dotenv-vault pull --dotenvMe it_e3811a4…
```

#### Generating

You can generate an IT token by adding an integration to an environment.
