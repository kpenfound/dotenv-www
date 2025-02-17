---
layout: docs
title: ".env File - Security"
redirect_from:
  - /env
---

##### Security

# .env File

The .env file format is central to good DSX and has been since it was [introduced by Heroku](https://12factor.net/) in 2012 and popularized by our [dotenv node module](https://www.npmjs.com/package/dotenv) (and other libraries) in 2013.

The .env file format starts where the developer starts - in development. It is added to each project but NOT committed to source control. This gives the developer a single secure place to store sensitive application secrets.

Can you believe that prior to introducing the .env file, almost all developers stored their secrets as hardcoded strings in source control. That was only 10 years ago!

#### Example

Here's an example of what a .env file looks like:

```
# example .env file
STRIPE_API_KEY=scr_12345
TWILIO_API_KEY=abcd1234
```

It is purposefully simple because, as security professionals, we know that complexity is the enemy of security.

You can read more about how it works [here](https://github.com/motdotla/dotenv) (or at other implementations [here](https://github.com/bkeepers/dotenv), [here](https://github.com/theskumar/python-dotenv), [here](https://github.com/vlucas/phpdotenv)). It is the gold standard for securing development secrets - proven and trusted by millions of developers around the world.

But the world has changed and developers manage secrets at far greater scale than a decade ago. Today it's difficult to securely share .env files between machines, environments, and team members. As a result, developers often share secrets over Slack, email, text message, and post-it notes. It's not scaleable and fraught with security risks. For a CTO or CSO it is a risk they should not take.

#### Extending .env

Luckily, that is changing. We have been extending the .env file format to support secure sharing.

The .env file format will still be at the center of security. But we have added two new extensions. They are not required. They are optional, but we highly recommend them for teams. They are the:

* [.env.vault](/docs/security/env-vault) extension
* [.env.me](/docs/security/env-me) extension

In the next set of security docs you can read about how these work alongside your .env files to significantly improve security. This is the next great leap forward in application secrets security, and like the original .env file format we have worked hard to minimize complexity in order to increase security.
