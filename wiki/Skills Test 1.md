## Overview

These are the general instructions for the first Skills Test in [our application process].

[our application process]: Process-Overview

## Before the Test

- We will schedule the test through Breezy.
- You will receive a Slack invite the evening before or the day of the test.
- At the start of the test, you will receive an invite to an empty GitHub repo.
- You will receive the product request for a web app prototype as a GitHub issue in that
  repo.

## Confidentiality

By proceeding with this skills test, you agree to keep the test content confidential and
not disclose it to any third party.

You are welcome to talk about your experience taking the test as long as what you share
would not advantage a future test taker.

- If you do **not** agree, stop taking the test now and notify the facilitator.
- If you **do** agree, acknowledge that in the Slack channel set up for this test.

## General Instructions

- You may use internet resources, including AI/LLMs, subject to the AI Assistance Method
  section below.
  - Part of what we evaluate is how wisely you use the tools available to you.
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
- The site should feel modern and helpfully interactive/dynamic, but it does not need to
  be a SPA.
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

Choose your AI assistance method before you start. The time limit depends on that choice.

- **Agentic:** 4 hours of working time (5 hours total)
- **AI-assisted:** 6.5 hours of working time (7.5 hours total)

Working time is the time limit for doing the project itself. The total time adds about 30
minutes up front for instructions/discussion and about 30 minutes at the end for PR
submission and `feedback.md`. Total time is also the maximum we will pay for the test.

Remember:

- Stay within the time limit for the method you chose.
- Make sure your final work is committed within that time limit.
- After that, submit your PR and create `feedback.md`.

We expect you to start promptly after receiving the test and work through it to
completion, with only a short break midway through if needed. After you submit your PR,
you may take a break before writing `feedback.md`. That time does not count against the
working-time limit.

## When Finished

After you make your final commit within the time limit:

- submit your PR
- create a `feedback.md` file in the repo
- include any feedback that may help our evaluation or improve the test/process

Time spent on the PR and `feedback.md` does not count against the test time limit.

## AI Assistance Method

Choose one AI assistance method for the entire test and tell us which one you are using.
We need this ahead of time to schedule the correct amount of time.

The AI assistance method you choose affects three things:

- what kind of AI help is allowed
- how much time you have
- what we will pay more attention to in our evaluation

The difference between the two methods comes down to what the AI is allowed to do.

- **AI-assisted**: AI is only advising you and you must manually type or paste the result
  yourself.
- **Agentic**: AI can directly write code in your editor or act on your workspace.

Also, if more than 50% of the code you write to address the product instructions
(excluding boilerplate) is pasted from AI output, we will treat your test as **Agentic**.

These examples are meant to be concrete, not exhaustive. If a tool or feature feels close
to the line, ask the facilitator **before** you use it.

### AI-assisted

With AI-assisted, you may use AI to advise you, explain things, brainstorm with you,
review code, or generate code/examples for you to read and manually apply yourself.

The key rule is this: the AI must **not** directly modify your workspace.

Allowed with AI-assisted:

- Browser chats such as ChatGPT, Claude, and similar tools
- A local or in-IDE AI chat tool that only answers questions or prints suggestions as text
- Copying and pasting code from an AI response into your editor yourself
- Asking AI to explain errors, compare approaches, suggest code examples, or review what
  you wrote

Not allowed with AI-assisted:

- Any AI feature that can directly create, edit, refactor, or apply changes to files in
  your repo
- In-IDE agent prompting or chat-to-edit workflows
- CLI coding agents
- AI-powered refactors or "apply this change" workflows
- AI autocomplete or inline completion
- Any similar feature that writes directly into your editor or workspace
- Having more than 50% of the code written to address the product instructions (excluding
  the boilerplate commit) generated by AI (i.e. through copy & paste).

### Agentic

With Agentic, you may use AI tools that can act on your workspace and write code for you.

This includes tools that can directly create or edit files, propose and apply patches,
refactor code in place, or otherwise make changes in your editor or repo.

Examples of tools/features allowed with Agentic:

- Local CLI coding agents
- In-IDE agent features
- Chat features that can apply edits to files
- AI refactors or code actions that change files
- AI autocomplete and inline completion
- Any other AI feature that writes directly into your editor or workspace

If you choose Agentic, you are still responsible for steering the tool, reviewing the
output, and verifying that what it produced is correct.

### How evaluation changes by method

We care about the same core outcomes in both methods. The difference is not the standard.
The difference is where we place more weight.

- With **AI-assisted**, we look more closely at your direct implementation work.
- With **Agentic**, we look more closely at how well you plan, steer, review, and verify
  the resulting work.

In either case, we evaluate:

- how well you understand and break down the request
- how well the app works; presence of bugs
- whether the app conforms to the product request
- whether the code is understandable and maintainable
- whether the code shows evidence of sound engineering and product judgment
- whether the code shows evidence of being well tested and verified

### Additional Notes

- We will use AI detection tools to evaluate how much of your submission is AI generated.
- Agentic artifacts like specs, steering docs, prompts, or plans should be submitted with
  the PR.
- If you use **Agentic**, or signed up for an AI provider's plan specifically to help with
  this assessment, we will pay you an extra $25 to help cover credits/tokens used.
  **Please request this reimbursement** through Breezy when it applies.
- We have seen good agentic results from [Augment Code's](https://www.augmentcode.com/)
  agents using GPT to plan/code and Opus to review at both stages. But, YMMV.
