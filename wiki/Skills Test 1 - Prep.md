## Overview

These are the general instructions for the first Skills Test in [our application process].

[our application process]: Process-Overview

## Before the Test

- We will schedule the test through Breezy.
- You will receive a Slack invite the evening before or the day of the test.
- At the start of the test, you will receive an invite to an empty GitHub repo.
- That repo will include the product request for the prototype you need to build.

## Confidentiality

By proceeding with this skills test, you agree to keep the test content confidential and
not disclose it to any third party.

You are welcome to talk about your experience taking the test as long as what you share
would not advantage a future test taker.

- If you do **not** agree, stop taking the test now and notify the facilitator.
- If you **do** agree, acknowledge that in the Slack channel set up for this test.

## General Instructions

- You may use any internet resource, including AI/LLMs, to help you solve the problem.
  - Using those resources well to save development time is part of what we are evaluating.
- You may not consult with other people during the test, except for the facilitator.
- Read the instructions carefully.
- Please ask questions whenever something is unclear or you want a quick read on the
  instructions.
  - You are not bothering us. That is what we are here for.
- Keep Slack open so we can communicate.
  - Installing the client and making sure notifications work is even better.
- Use the GitHub repo to share your solution with us.

## App Template

You may prepare a base project or template ahead of the test. It should remove setup
friction, not pre-build the product.

Do:

- Use code generation utilities to lay down the app basics.
  - Examples: a Django project generator, `create-react-app`, Vite, etc.
- Set up standard dev tooling such as `mise`, `uv`, linting, formatting, and test config.
- Set up the basic frontend/backend structure and connection points.
- Keep the template generic and reusable.

Don't:

- Anticipate product features and build them ahead of time.
- Add libraries, integrations, or setup for anticipated project needs that would not
  belong in a generic base template.
- Include product-specific models, workflows, UI, business logic, or other domain code.
- Turn the template into a partial solution.

In short: it should remain a skeleton that removes setup friction, **not a head start on
the actual assignment.**

## Commits / Branches

- If you use a boilerplate app setup or template, commit that **directly to the main
  branch**.
  - This is usually a large, mostly generated commit, and we do not want that noise in the
    main PR.
- Put the features and functionality you add on a feature branch.
  - Open a PR from that feature branch for easier review.

## Technologies

### Backend

- Use Python.
- Use whatever libraries or framework will make you most productive.

### Frontend

- Use whatever you are most comfortable and productive with for the test.
- The site should feel modern and helpfully dynamic, but it does not need to be a SPA.
- We slightly prefer solutions that do not require a front-end build step because of
  dependency churn and supply chain risk.
  - That said, your productivity matters more. Choose what will make you most productive.

### Dev Tools

- Use `mise` and `uv`.
- Another developer with those tools installed should be able to fully run and test the
  application without manually installing other apps, libraries, or tooling.
- This also helps keep CI relatively simple.

### Services

- Prefer defining services such as databases in Docker Compose.

### Third-Party Services

- Generally avoid third-party services.

## Time Limits

The test time limit is **4 hours**.

Time spent reading, understanding, or discussing the instructions **does not count toward
that limit**.

- The time limit is 4 hours. Not 4:05 or 4:15.
- Make sure your final work is committed within the time limit.
- You may take additional time after that to submit the PR and update `feedback.md`.

We expect you to start promptly after receiving the test and work through it to
completion, with only a short break midway through if needed.

We know this is not quite how real-world development works. We use the time limit to keep
evaluations consistent across candidates.

## When Finished

After you make your final commit within the time limit:

- submit your PR
- create a `feedback.md` file in the repo
- include any feedback that may help our evaluation or improve the test/process

Time spent on the PR and `feedback.md` does not count against the test time limit.
