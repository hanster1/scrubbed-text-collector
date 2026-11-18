# Scrubbed Text Collector

Collect your text history on your own computer, use a local AI model to filter sensitive messages, and give your chosen AI assistant access to the archive you approve. This repository is a setup guide. Your setup agent builds the collector for your phone, messaging app, and computer.

This README is for you. [PLAYBOOK.md](PLAYBOOK.md) is the guide your setup agent follows.

## What you'll set up

1. **Collect your texts privately.** Save as much history as your messaging service makes available in a local `collected-texts` folder. Your setup agent will check how far back it goes and report any gaps.
2. **Filter them on your computer.** Use a local language model and filtering rules to keep sensitive content out of the `scrubbed-texts` folder. Check the results privately before sharing. A filter can miss sensitive details, so share only what you're comfortable letting your chosen service see.
3. **Ask questions about your texts.** Connect only the approved `scrubbed-texts` folder to an AI assistant that can search it. Depending on what your app and account support, you can use ChatGPT, Claude, Grok, or another assistant.
4. **Keep the archive current.** Schedule collection and filtering, then check that a later update reaches the app you use to ask questions.

## Choose a computer

Use a computer you can leave on and awake, such as a home server or a spare desktop. While it's asleep or off, the archive stops updating. Your assistant can see new texts once collection, filtering, and any sync have run again.

Collection depends on your phone and messaging app. Even if the setup agent runs on your computer, your messaging service may require another device or may offer only part of your history.

## Setup overview

1. Install a setup agent such as Codex or Claude Code if you need one.
2. Create a folder called `scrubbed-text-collector` and launch the agent there.
3. Paste the setup prompt below. Your agent will walk you through choices such as what to collect, what to withhold, and where you want to ask questions.

## Detailed instructions

### 1. Install an agent CLI

A command-line interface (CLI) lets you run your setup agent in a terminal so it can do the technical work on your computer. Choose **one** agent and use an account supported by its provider. If you already have one installed, skip to step 2.

#### Mac

Press **Command-Space**, type **Terminal**, and press **Return**. Run the install command for the agent you chose.

**Codex**

```sh
curl -fsSL https://chatgpt.com/codex/install.sh | sh
```

**Claude Code**

```sh
curl -fsSL https://claude.ai/install.sh | bash
```

#### Windows

Open **Start**, type **PowerShell**, and open it. Run the install command for the agent you chose.

**Codex**

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://chatgpt.com/codex/install.ps1 | iex"
```

**Claude Code**

```powershell
irm https://claude.ai/install.ps1 | iex
```

For Linux, other installation methods, or help signing in, see the official [Codex quickstart](https://github.com/openai/codex#quickstart) or [Claude Code quickstart](https://code.claude.com/docs/en/quickstart).

### 2. Create the project folder and launch the agent

Open a fresh Terminal window on Mac or Linux, or PowerShell on Windows. Run the block for the agent you chose. If the folder already exists, skip the `mkdir` line. Follow the agent's sign-in prompts if this is your first launch.

**Codex**

```text
cd ~
mkdir scrubbed-text-collector
cd scrubbed-text-collector
codex
```

**Claude Code**

```text
cd ~
mkdir scrubbed-text-collector
cd scrubbed-text-collector
claude
```

### 3. Paste the setup prompt

Paste this into the agent after it opens.

```text
Read https://raw.githubusercontent.com/hanster1/scrubbed-text-collector/main/PLAYBOOK.md and follow it to set up Scrubbed Text Collector on this computer. Walk me through pairing, privacy choices, and a private review before sharing. Keep originals and credentials outside this agent session. Verify what history is available and test that a later update reaches the app I use to ask questions.
```
