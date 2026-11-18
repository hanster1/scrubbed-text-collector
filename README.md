# Scrubbed Text Collector

These instructions will walk you through how to scrub your texts of sensitive information using a local LLM running on your own computer so that you can securely give your text history to Claude, ChatGPT, Muse, or Grok without exposing sensitive information.

This README is instructions for humans. The [PLAYBOOK](PLAYBOOK.md) is instructions for agents.

By the end of your setup you will have done the following:

1. Collect your full text history into a `collected-texts` folder on your computer without exposing any of these texts to cloud agents.
2. Scrub your texts of sensitive information using a local LLM that runs on your computer and saves your scrubbed text archive into a `scrubbed-texts` folder.
3. Connect your cloud agents of choice to the `scrubbed-texts` folder to get intelligent answers about your text history.
4. Keep your text collection and scrubbing running on your own computer so that your cloud agents always have access to your latest texts.

## A Home Server

Your scrubbed text collector is only working while your computer is on. Therefore, it is best to go through this setup on a computer that you can leave on. If the computer gets turned off, then text collection and scrubbing gets turned off, which means your agent is temporarily blind to your latest texts until your computer is turned back on.

## Setup Overview

1. If you don’t already have the agent CLI of your choice installed on your computer, install it.
2. Create a new project folder on your computer called `scrubbed-text-collector`.
3. Run your agent CLI from the `scrubbed-text-collector` project folder.
4. Paste the following prompt to your agent:

   ```text
   Follow https://github.com/hanster1/scrubbed-text-collector to set up scrubbed-text-collector on this computer.
   ```

## Detailed Instructions

### Install an Agent CLI

An agent CLI is an interface for Claude or ChatGPT to run on your computer and make changes to your computer using a command line interface (CLI). You need to already have a subscription with Claude or ChatGPT to use their agent CLI.

#### For Mac

Press Command-Space, type Terminal, and press Return. Paste one install command.

**Codex:**

```sh
curl -fsSL https://chatgpt.com/codex/install.sh | sh
```

**Claude Code:**

```sh
curl -fsSL https://claude.ai/install.sh | bash
```

#### For Windows

Open Start, type PowerShell, and open it. Paste one install command.

**Codex:**

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://chatgpt.com/codex/install.ps1 | iex"
```

**Claude Code:**

```powershell
irm https://claude.ai/install.ps1 | iex
```

For installation help, see the official [Codex](https://learn.chatgpt.com/docs/codex/cli) or [Claude Code](https://code.claude.com/docs/en/quickstart) instructions.

### Create a project folder and launch your agent

Open Terminal on Mac or PowerShell on Windows. Paste the commands for your chosen agent to create a new `minbox-setup` folder and launch it.

**Codex:**

```text
cd ~
mkdir minbox-setup
cd minbox-setup
codex
```

**Claude Code:**

```text
cd ~
mkdir minbox-setup
cd minbox-setup
claude
```
