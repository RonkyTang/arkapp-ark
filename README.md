<!--
  Deliverable, not this repo's README.

  Copy this file into the public repo (suggested: github.com/arkapp/ark) as its
  README.md. That repo carries documentation and issues only; Ark is closed
  source, so no application code goes there.

  Why it exists: github.com pages rank well and are often the first result for a
  tool's name, and a public issue tracker keeps producing indexable content. See
  documents/GTM/SEO_OFFSITE_CHECKLIST.md, section P0.

  Every claim below must stay consistent with
  documents/GTM/website/WEBSITE_CONTENT_RATIONALE.md section 5: no unverified
  numbers, no competitor comparisons without a source and a date.

  Translations live in README.zh-CN.md and README.ja.md. The three files carry
  the same claims, sections, and links; when one changes, change all three.
-->

**English** · [简体中文](README.zh-CN.md) · [日本語](README.ja.md)

# Ark — an AI-native terminal and SSH client

Ark is an SSH client and terminal for remote servers, with an AI agent that
works from the machine you are already connected to. The terminal, SFTP file
transfer, and server state share one real connection, so the agent starts from
live facts instead of asking you to describe your setup.

**macOS 11+ (Apple Silicon and Intel) · Windows x64 · Free plan available**

[**Download Ark**](https://arkapp.ai/#download) ·
[What the agent does](https://arkapp.ai/ai-ssh-client) ·
[macOS](https://arkapp.ai/ssh-client-mac) ·
[Windows](https://arkapp.ai/ssh-client-windows) ·
[Changelog](https://arkapp.ai/changelog)

> This repository holds documentation and the public issue tracker. Ark itself is
> closed source, so no application code is published here. Bug reports and
> feature requests are welcome in [Issues](../../issues).

---

## What Ark is

Most AI terminal tools open a chat box and wait for you to explain the
background. Ark reads the context it already has: the host you connected to, the
identity you are using, the current directory, running services, listening
ports, and the output you just saw.

When something needs more than a single command, you state the goal. The agent
gathers evidence on the server, proposes a next step, waits for your
confirmation before changing anything, and then verifies the result.

It is a complete SSH client on its own. If you never turn on the agent, Ark is
still a terminal you can work in every day.

## Features

- **Terminal** — shell sessions, split panes, history, and completion over one
  real SSH connection.
- **SFTP file transfer** — browse, upload, and download beside the terminal
  instead of switching to a separate app. Transfer queues can be paused,
  resumed, and retried.
- **Server state in view** — identity, resources, services, listening ports, and
  watch items, visible before you decide what to do.
- **SSH config import** — existing host settings are read in, so addresses,
  users, and authentication details do not need re-entering.
- **Unlimited connected hosts** — host count is not limited by plan.
- **AI agent** — reads live server state, follows evidence across steps, and
  separates what it verified from what it is still unsure about.
- **Bring your own model key** — configure custom models so the provider and the
  API key stay under your control.
- **Interface languages** — English, 简体中文, 日本語.

## Control and credentials

The point of letting an agent touch a real server is that the boundaries are
explicit. These are product behaviours, not options you have to remember to
enable:

- No material change happens without an explicit confirmation from you, and a
  confirmation authorizes only the operation in front of you.
- Before a change, Ark shows the server, the identity, the target, the full
  command, the expected impact, and how the result will be verified.
- SSH private keys, passwords, and your custom model API keys stay on your
  device. The agent does not read them.
- You can stop a run and finish the work in the CLI at any point.
- Execution success, technical verification, and business health are reported
  separately, so "the command ran" is never presented as "the problem is fixed".

## Install

Download the installer for your system from
[arkapp.ai](https://arkapp.ai/#download). Sign-in is required to download.

| Platform | Requirement | Installer |
| --- | --- | --- |
| macOS | 11 (Big Sur) or later, Apple Silicon or Intel | signed disk image |
| Windows | 10 or later, x64 | NSIS installer (`.exe`) |

Ark checks for new versions and can install updates from inside the app, so you
do not need to download manually after the first install.


## FAQ

**Is Ark an SSH client or an AI assistant?**
Both. It is a complete SSH client and terminal you can use on its own, plus an
agent that works from the server you already connected to.

**Can I use Ark without the AI features?**
Yes. The Free plan covers SSH and CLI sessions, SFTP file transfer, unlimited
connected hosts, and local history.

**Where are my SSH keys stored?**
On your device. Private keys, passwords, and custom model API keys are not
uploaded.

**Which models does Ark use?**
You bring your own API key, so the provider and the key stay yours.

**Is Linux supported?**
Not yet. macOS and Windows x64 are the published targets.

## Feedback and contact

- Bugs and feature requests: [Issues](../../issues)
- Email: <official@arkapp.ai>
- [Terms of Service](https://arkapp.ai/#legal-tos) ·
  [Privacy Policy](https://arkapp.ai/#legal-privacy)

---

Ark is released English-first for users in the United States. It is not promoted
or listed in mainland China app stores; access to the website is not blocked.
