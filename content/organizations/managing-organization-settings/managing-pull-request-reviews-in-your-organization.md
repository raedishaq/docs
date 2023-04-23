![background](https://github.com/github/docs/assets/131593783/cbba4d2e-c1af-4b50-b2ee-884a6b01fee5)
![floppy png](https://github.com/github/docs/assets/131593783/b07c2c79-7156-414a-bbd5-1c194d396b63)
![iphone](https://github.com/github/docs/assets/131593783/e9313f3d-5f75-4a0e-a1a4-5d03d748de67)
![laptop](https://github.com/github/docs/assets/131593783/06dc18eb-3862-4f70-a13c-ad0514aba4be)
![pendrive](https://github.com/github/docs/assets/131593783/b03b9086-a42a-4d87-a23d-b43500088c2e)
![pixel](https://github.com/github/docs/assets/131593783/9a19ae0f-f69a-4edc-9f93-8c6af698f828)
![tablet](https://github.com/github/docs/assets/131593783/eb46d9f3-89b9-4985-a9c6-3e4b26f56389)
---
title: Managing pull request reviews in your organization
intro: You can limit which users can approve or request changes to a pull requests in your organization.
versions:
  feature: pull-request-approval-limit
permissions: Organization owners can limit which users can submit reviews that approve or request changes to a pull request.
topics:
  - Organizations
  - Pull requests
shortTitle: Manage pull request reviews
---

## About code review limits

By default, in public repositories, any user can submit reviews that approve or request changes to a pull request.

You can limit who is able to approve or request changes to pull requests in public repositories owned by your organization. After you enable code review limits, anyone can comment on pull requests in your public repositories, but only people with explicit access to a repository can approve a pull request or request changes.

You can also enable code review limits for individual repositories. If you enable or limits for your organization, you will override any limits for individual repositories owned by the organization. For more information, see "[AUTOTITLE](/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/managing-pull-request-reviews-in-your-repository)."

## Managing code review limits

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
1. In the "Access" section of the sidebar, click **{% octicon "report" aria-label="The report icon" %} Moderation**.
1. Under "{% octicon "report" aria-hidden="true" %} Moderation", click **Code review limits**.
1. Review the information on screen.
1. Manage code review limits.
  - To limit reviews to those with explicit access, click **Limit review on all repositories**.
  - To remove the limits from every public repository in your organization, click **Remove review limits from all repositories**.
