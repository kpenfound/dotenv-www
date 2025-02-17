---
layout: docs
title: "Adding Teammates - Tutorial"
parent: Docs
redirect_from:
  - /docs/getting-started/with-adding-teammates
---

##### Tutorial

# Adding Teammates

Use dotenv-vault to add teammates - so they can securely push and pull changes to your .env file. No more sharing .env files over insecure channels like Slack and email.



#### 1. Run dotenv-vault open

Open terminal, enter your project's root directory (where your .env.vault file is), and run dotenv-vault open.

```
$ npx dotenv-vault open
```

{% include helpers/screenshot.html url="https://res.cloudinary.com/dotenv-org/image/upload/c_scale,w_900/v1659628450/Screen_Shot_2022-08-04_at_8.53.10_AM_cgkgkk.png" %}

<small>FYI: Not a developer? You can navigate to this page by visiting ui.dotenv.org.</small>

#### 2. Click Team Dropdown

Click the 'Team' dropdown button and then click 'Manage access'.

{% include helpers/screenshot.html url="https://res.cloudinary.com/dotenv-org/image/upload/c_scale,w_900/v1659647516/Screen_Shot_2022-08-04_at_2.10.17_PM_bdiezm.png" %}

#### 3. Click Add Teammate

On the next page, click 'Add Teammate'.

{% include helpers/screenshot.html url="https://res.cloudinary.com/dotenv-org/image/upload/c_scale,w_900/v1659648001/Screen_Shot_2022-08-04_at_2.13.27_PM_rxvyll.png" %}

#### 4. Enter Teammate's Email Address

Enter your teammate's email address and click 'Add teammate'.

{% include helpers/screenshot.html url="https://res.cloudinary.com/dotenv-org/image/upload/c_scale,w_900/v1659648252/Screen_Shot_2022-08-04_at_2.15.11_PM_l9rzrl.png" %}
{% include helpers/screenshot.html url="https://res.cloudinary.com/dotenv-org/image/upload/c_scale,w_900/v1659657654/Screen_Shot_2022-08-04_at_4.58.59_PM_exusnj.png" %}

#### 5. Tell Your Teammate to Check Their Email

They will receive an email with instructions to run dotenv-vault pull. They can also choose to log in.

{% include helpers/screenshot.html url="https://res.cloudinary.com/dotenv-org/image/upload/c_scale,w_900/v1659657800/Screen_Shot_2022-08-04_at_2.17.49_PM_djym8s.png" %}

#### 6. Teammate: Run dotenv-vault login

Your teammate visits their terminal, enters the project directory (which they've already git-cloned via a service like GitHub or GitLab), and runs dotenv-vault login.

```
$ npx dotenv-vault login
```

#### 7. Teammate: Click Login

On the next screen, your teammate should follow the login process and click 'Log in'.

#### 8. Teammate: View .env.me file (optional)

Your teammate now has their own .env.me file (on their machine only) in the root of the project. The .env.me file uniquely authorizes them to access the project's shared .env file. Think of it like a unique SSH key at GitHub.

Run ls -al to view it.

```
$ ls -al
Jul 28 17:54 .
Jul 27 13:46 ..
Jul 28 18:11 .env.me
Jul 28 18:09 .env.vault
Jul 28 17:54 .gitignore
Jul 27 14:49 index.js
...
```

{% include helpers/screenshot.html url="https://res.cloudinary.com/dotenv-org/image/upload/c_scale,w_900/v1659128781/dotenv-me_bsffi2.png" %}

#### 9. Teammate: Run dotenv-vault pull

Your teammate returns to their terminal and runs dotenv-vault pull.

```
$ npx dotenv-vault pull

remote:   Securely pulling... done
remote:   Securely pulled development (.env)
```

{% include helpers/screenshot.html url="https://res.cloudinary.com/dotenv-org/image/upload/v1659659716/teammate-pull_zlk3hr.gif" %}

#### 10. Teammate: Run dotenv-vault push (optional)

Your teammate can edit the .env file and push changes with dotenv-vault push.

```
$ npx dotenv-vault push

remote:   Securely pushing (.env)... done
remote:   Securely pulled development (.env)
```
{% include helpers/screenshot.html url="https://res.cloudinary.com/dotenv-org/image/upload/v1659660333/teammate-push_m2r46u.gif" %}

#### 11. You: Run dotenv-vault pull (optional)

Pull the changes your teammate made with dotenv-vault pull.

```
$ npx dotenv-vault pull

remote:   Securely pulling... done
remote:   Securely pulled development (.env)
```
{% include helpers/screenshot.html url="https://res.cloudinary.com/dotenv-org/image/upload/v1659660592/teammate-pull_g5o4px.gif" %}

That's it! Thanks for using dotenv-vault with your teammates and friends.
