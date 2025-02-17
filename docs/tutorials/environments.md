---
layout: docs
title: "Managing Environments - Tutorial"
parent: Docs
redirect_from:
  - /docs/getting-started/with-multiple-environments
---

##### Tutorial

# Managing Environments

Use dotenv-vault to manage your environment variables across multiple environments - like production and staging.

#### Run dotenv-vault open

Open terminal, enter your project's root directory (where your .env.vault file is), and run dotenv-vault open.

```
$ npx dotenv-vault open
```

{% include helpers/screenshot.html url="https://res.cloudinary.com/dotenv-org/image/upload/c_scale,w_900/v1659628450/Screen_Shot_2022-08-04_at_8.53.10_AM_cgkgkk.png" %}

<small>FYI: Not a developer? You can navigate to this page by visiting ui.dotenv.org.</small>

#### Click Environment Dropdown Button

Click the environment dropdown button labeled 'development' and then click 'production'.

{% include helpers/screenshot.html url="https://res.cloudinary.com/dotenv-org/image/upload/c_scale,w_900/v1659628722/Screen_Shot_2022-08-04_at_8.53.16_AM_pukxin.png" %}

#### Edit Your Production Environment Variables

Click the edit icon next to the environment variable you want to edit.

{% include helpers/screenshot.html url="https://res.cloudinary.com/dotenv-org/image/upload/c_scale,w_900/v1659630619/Screen_Shot_2022-08-04_at_9.01.21_AM_vcrkkd.png" %}

<small>FYI: You'll notice that your production environment variable names are already setup but with blank values. This is by design. Each time you add an environment variable to your .env file it gets copied over to your other environments.</small>

#### Set the Production Value

Enter a value and click 'Save changes'.

{% include helpers/screenshot.html url="https://res.cloudinary.com/dotenv-org/image/upload/c_scale,w_900/v1659630861/Screen_Shot_2022-08-04_at_9.24.43_AM_hqarvz.png" %}

#### Pull .env.production

Return to terminal and run dotenv-vault pull production.

```
$ npx dotenv-vault pull production

remote:   Securely pulling production... done
remote:   Securely pulled production (.env.production)
```

#### View .env.production file

Run ls -al to view it.

```
$ ls -al
Jul 28 17:54 .
Jul 27 13:46 ..
Jul 27 14:51 .env
Jul 27 14:51 .env.me
Jul 28 18:09 .env.vault
Jul 28 18:09 .env.production
Jul 28 17:54 .gitignore
...
```
{% include helpers/screenshot.html url="https://res.cloudinary.com/dotenv-org/image/upload/c_scale,w_900/v1659631492/Screen_Shot_2022-08-04_at_9.44.05_AM_fqavup.png" %}

#### Push .env.production file (optional)

Prefer to manage your non-development environments with the cli? Edit .env.production and run dotenv-vault push production.

```
$ npx dotenv-vault push production

remote:   Securely pushing production (.env.production)... done
remote:   Securely pushed production (.env.production)
```
{% include helpers/screenshot.html url="https://res.cloudinary.com/dotenv-org/image/upload/v1659633035/push-production_gdegey.gif" %}
{% include helpers/screenshot.html url="https://res.cloudinary.com/dotenv-org/image/upload/c_scale,w_900/v1659633123/Screen_Shot_2022-08-04_at_10.11.25_AM_llgwx9.png" %}

That's it! Thanks for using dotenv-vault with multiple environments.
