<!--
  Aligned copy for GitHub README claims. 2026-09-08 product decision: do not
  create a separate github.com/arkapp/ark. The currently public git README is
  already used for SEO.

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

**macOS 12+ (Apple Silicon and Intel) · Windows x64 · Free plan available**

[**Download Ark**](https://arkapp.ai/#download) ·
[Mac App Store](https://apps.apple.com/app/ark-ssh/id6803574965?mt=12) ·
[What the agent does](https://arkapp.ai/ai-ssh-client) ·
[macOS](https://arkapp.ai/ssh-client-mac) ·
[Windows](https://arkapp.ai/ssh-client-windows) ·
[Changelog](https://arkapp.ai/changelog)

> This repository holds documentation and the public issue tracker. Ark itself is
> closed source, so no application code is published here. Bug reports and
> feature requests are welcome in [Issues](https://github.com/RonkyTang/napoleon/issues).

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
- **Local experience cards** — after a task, you can save distilled notes on
  this device. They stay encrypted here, bound to your account and this host,
  and are used only as investigation leads.
- **Interface languages** — English, 简体中文, 日本語.

## Control and credentials

The point of letting an agent touch a real server is that the boundaries are
explicit. These are product behaviours, not options you have to remember to
enable:

- Interactive Agent changes require your explicit confirmation for each operation. Scheduled tasks run only within the scope you previously saved and authorized.
- Before a change, Ark shows the server, the identity, the target, the full
  command, the expected impact, and how the result will be verified.
- SSH private keys, passwords, and your custom model API keys stay on your
  device. The agent does not read them. Local-network pairing copies them between
  your devices and does not go through Ark's cloud.
- You can stop a run and finish the work in the CLI at any point.
- Execution success, technical verification, and business health are reported
  separately, so "the command ran" is never presented as "the problem is fixed".

## Install

Download the installer for your system from
[arkapp.ai](https://arkapp.ai/#download). Outside mainland China, Mac can also
install from the
[Mac App Store](https://apps.apple.com/app/ark-ssh/id6803574965?mt=12).

| Platform | Requirement | Installer |
| --- | --- | --- |
| macOS | 12 (Monterey) or later, Apple Silicon or Intel | signed disk image from the website, or [Mac App Store](https://apps.apple.com/app/ark-ssh/id6803574965?mt=12) outside mainland China |
| Windows | 10 or later, x64 | NSIS installer (`.exe`) |

The website build checks for new versions and can install updates from inside the
app. The Mac App Store build updates through the store.

## Pricing

| Plan | Price | Includes |
| --- | --- | --- |
| Free | $0 | Sign-in, SSH / CLI sessions, SFTP file transfer, unlimited connected hosts, local history, multi-device sign-in (no sync) |
| Basic | $1.99 / month | Everything in Free, the agent and single-server cockpit, custom models with your own API key, local experience cards (encrypted on this device, per host) |
| Pro | $4.99 / month | Everything in Basic, plus local scheduled tasks and iOS / Android companions that pair over the local network (browse, upload, transfer, preview remote images and video, and confirm-to-delete). The iOS app is not yet listed in the App Store. Android is not on Google Play; the official APK is not published yet. Multi-device data sync, cross-server work, MCP and Skills remain planned. |

Register by November 30, 2026 to receive a free Basic trial. The promotion
does not auto-renew or charge you. Without a paid subscription the account
returns to Free.

Paid plans are monthly and auto-renew until you cancel. You can cancel
anytime; the current period stays active, then the account returns to Free.
Website and direct-download purchases go through Stripe. The Mac App Store
build follows Apple’s subscription rules and shows store prices. Model
usage is billed by your provider, not by Ark.

## FAQ

**Is Ark an SSH client or an AI assistant?**
Both. It is a complete SSH client and terminal you can use on its own, plus an
agent that works from the server you already connected to.

**Can I use Ark without the AI features?**
Yes. The Free plan covers SSH and CLI sessions, SFTP file transfer, unlimited
connected hosts, local history, and multi-device sign-in without cloud sync.

**Where are my SSH keys stored?**
SSH private keys and passwords stay on your device. Your custom model API key is sent only as needed to the model endpoint you configure and is not uploaded to Ark. Local-network pairing copies them between your devices and does not
go through Ark's cloud.

**Which models does Ark use?**
You bring your own API key, so the provider and the key stay yours.

**Is Linux supported?**
Not yet. The published downloads are macOS and Windows x64. macOS is also on
the Mac App Store outside mainland China. Pro includes iOS and Android
companions that pair over the local network; iOS is not listed in the App
Store yet, and the official Android APK is not published yet.

**How do subscriptions and cancellation work?**
Paid plans are monthly and auto-renew until you cancel. You can cancel
anytime; the current period stays active, then the account returns to Free.
Website and direct-download purchases go through Stripe. The Mac App Store
build follows Apple’s subscription rules. Model usage is billed by your
provider, not by Ark.

## Feedback and contact

- Bugs and feature requests: [Issues](https://github.com/RonkyTang/napoleon/issues)
- Email: <official@arkapp.ai>
- [Terms of Service](https://arkapp.ai/#legal-tos) ·
  [Privacy Policy](https://arkapp.ai/#legal-privacy)

---

Ark is available worldwide. The default language is English, with Simplified
Chinese and Japanese. It is not promoted or listed in mainland China app
stores; access to the website and use of the product are not blocked.
