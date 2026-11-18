# Scrubbed Text Collector

These instructions will walk you through collecting and filtering your texts on your own computer. Claude, ChatGPT, Muse, or Grok can search the archive you approve.

This README is instructions for humans. The [PLAYBOOK](PLAYBOOK.md) is instructions for agents.

### By the end of your setup you will have done the following:

1. Collect the full text history your messaging service makes available into a `collected-texts` folder on your computer.
2. Filter your texts with the option you chose and save the archive you approve into a `scrubbed-texts` folder.
3. Connect your cloud agents of choice to the `scrubbed-texts` folder to get intelligent answers about your text history.
4. Keep your text collection and scrubbing running on your own computer so that your cloud agents can access your latest scrubbed texts after each update.

## Home Server

Your scrubbed text collector is only working while your computer is on. Therefore, it is best to go through this setup on a computer that you can leave on. If the computer gets turned off, then text collection and scrubbing gets turned off, which means your agent is temporarily blind to your latest texts until your computer is turned back on.

## Get Started

1. Run Claude Code or Codex on your computer.
2. Paste this prompt for your agent:

   ```text
   Create a folder called scrubbed-text-collector and use it as the working
   directory for this setup. Follow the playbook at
   https://github.com/hanster1/scrubbed-text-collector/blob/main/PLAYBOOK.md
   to set up a scrubbed text archive on this computer. Walk me through the
   choices and handle the setup steps you can.
   ```

## Choose how to filter your texts

- **Private setup with a local LLM (default).** Use a model on your computer to help filter sensitive content based on what you choose to exclude. Your original messages stay on your computer. Cloud agents can access only the scrubbed archive you approve.
- **Simple cleanup with Codex or Claude Code.** Let your setup agent read and filter your texts for things like two-factor codes and spam. Your texts are processed by the agent’s cloud provider.

## Loom Videos, Media, and More

Texts are included by default, but your scrubbed text archive can also include Loom video transcripts, images, and more. Just ask your agent to help you include those parts of your texts into your scrubbed-text archive.
