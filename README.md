# Scrubbed Text Collector

These instructions will walk you through how to scrub your texts of sensitive information using a local LLM running on your own computer. Claude, ChatGPT, Muse, or Grok can search the scrubbed archive you approve. The original messages stay on your computer, outside the cloud agents' access.

This README is instructions for humans. The [PLAYBOOK](PLAYBOOK.md) is instructions for agents.

### By the end of your setup you will have done the following:

1. Collect the full text history your messaging service makes available into a `collected-texts` folder on your computer without exposing any of these texts to cloud agents.
2. Scrub your texts of sensitive information using a local LLM that runs on your computer and saves your scrubbed text archive into a `scrubbed-texts` folder.
3. Connect your cloud agents of choice to the `scrubbed-texts` folder to get intelligent answers about your text history.
4. Keep your text collection and scrubbing running on your own computer so that your cloud agents can access your latest scrubbed texts after each update.

Your setup agent will also ask whether you want to include transcripts of Loom videos shared in your texts. Text messages are the default. Loom transcripts are added only if you choose to enable them.

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
5. Ask your agent to flag setup problems and prepare a report that can improve the instructions for other agents. Review the report before it’s posted.

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

Open Terminal on Mac or PowerShell on Windows. Paste the commands for your chosen agent to create a new `scrubbed-text-collector` folder and launch it.

**Codex:**

```text
cd ~
mkdir scrubbed-text-collector
cd scrubbed-text-collector
codex
```

**Claude Code:**

```text
cd ~
mkdir scrubbed-text-collector
cd scrubbed-text-collector
claude
```
