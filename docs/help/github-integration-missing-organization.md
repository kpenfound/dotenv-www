---
layout: docs
title: "GitHub Integration Missing Organization - Help"
redirect_from:
  - /docs/help/github_integration_missing_organization
---

##### Help

#### GitHub Integration Missing Organization

**Problem:** *I don't see my organization in the dropdown list of GitHub organizations. It should be there.*

**Context:** This is relatively common. It happens when you add a new organization to your GitHub - after having already granted Dotenv access to GitHub. For security reasons, GitHub does not automatically grant access to the new organization. Luckily, it's easy to fix.

**Solution:**

1. Go to Github Settings > Applications > [Authorized OAuth Apps](https://github.com/settings/applications).
2. Scroll until you find <strong>Dotenv.org</strong>
3. Click <strong>Dotenv.org</strong>
4. On the next page, find the list of GitHub organizations
5. Click the <strong>Grant</strong> button for each organization that needs access.

Thank you for using Dotenv. Need further help? Email us at [support@dotenv.org](support@dotenv.org).
