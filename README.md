# Start From Scratch. Use Arch. Let AI Do The Heavy Lifting.

*A manifesto for the impatient developer who refuses to compromise*

---

## The Conventional Wisdom Is Wrong

Everyone tells you the same thing: "Just use Ubuntu. Use a preconfigured dotfiles repo. Don't waste time on setup."

Bullshit.

That advice made sense in 2015. It's catastrophically wrong in 2026.

Here's what I did this morning: I booted a fresh Arch Linux install at 1:21 AM. By 6:00 AM, I had a fully configured Hyprland desktop with vim-style keybindings, 60+ development fonts, a screenshot tool with live OCR, clipboard history, auto-lock, Neovim with LSP, and every dev tool I need.

**4 hours and 38 minutes.** From nothing to a development environment that's *exactly* what I want.

Not someone else's dotfiles. Not Ubuntu's idea of sensible defaults. Not what some "Linux influencer" thinks you need. *Mine.*

---

## What Actually Got Done

Let me be concrete. This isn't hypothetical productivity porn from someone who spends more time tweeting about productivity than actually producing anything:

- **Full Hyprland Wayland Compositor** - Configured from scratch with waybar, wofi, dunst
- **60+ Nerd Fonts** - FiraCode, JetBrains Mono, Cascadia Code, Iosevka, you name it
- **Vim-style Everything** - HJKL for window focus, move, resize. Arrow keys are for people who also use their mouse to select text.
- **macOS-style Screenshots with OCR** - `Super+Shift+6` selects a region and extracts text. In 2026. On Linux. While Mac users pay $3000 for the privilege.
- **Clipboard History** - `Super+V` brings up a searchable history. Obviously. It's not 2008.
- **Power Management** - Auto-lock at 5 min, screen off at 10 min, proper sleep handling
- **Neovim** - LSP, completion, telescope. Not VS Code. I'm not a tourist.
- **Claude Code CLI** - AI pair programmer in the terminal
- **GitHub CLI** - SSH auth, ready to ship

Ten significant accomplishments. Not "I installed VS Code and changed the theme to Dracula like everyone else on r/unixporn."

---

## The Secret: AI Changed Everything

Here's why the old advice is dead: **AI assistants are absurdly good at system configuration now.**

I didn't memorize Hyprland syntax. I didn't dig through wiki pages written by people who assume you already know everything. I didn't debug why my screenshot script wasn't working with Wayland's clipboard while half of Stack Overflow tells me to use xclip like it's still 2015.

I described what I wanted. Claude figured out the implementation.

```
"Add vim-style HJKL keybindings for moving windows"
"Make Super+Shift+6 select a region and OCR the text to clipboard"
"Configure hypridle to lock at 5 minutes and screen off at 10"
```

Three sentences. Three features. Done correctly the first time.

Meanwhile, you're on page 47 of a forum thread from 2019 where the solution involves compiling something from source and the last reply is "nvm fixed it" with no explanation.

---

## Why Arch Specifically?

Because Arch gives you nothing. And that's the point.

Ubuntu gives you someone else's opinions pre-installed. Canonical's. A company that thought putting Amazon search in your desktop was a good idea. A company that spent years pushing Snap packages that take 45 seconds to launch. Those are the people making decisions for you.

Pop!_OS gives you System76's workflow assumptions. Great if you're the exact person they imagined. Useless if you're not.

Fedora is Red Hat's testing ground. You're doing QA for free.

Mint is for your parents.

Arch gives you a blank canvas. You install exactly what you need. Nothing you don't. No snap. No flatpak unless you want it. No "Ubuntu Pro" nag screens. No decisions made by committees who've never seen your workflow.

When you combine that clean slate with an AI that can implement whatever you describe, you get something unprecedented: **a truly custom system built in hours instead of weeks.**

The old tradeoff was:
- Custom = slow and painful
- Fast = accept someone else's defaults

That tradeoff is dead. Custom AND fast is now possible. The people still recommending Ubuntu are giving you advice from a world that no longer exists.

---

## The Workflow

Here's how it actually works:

1. **Install Arch** - Use `archinstall`, takes 10 minutes. If you can't handle that, maybe stick to ChromeOS.
2. **Install your AI tool** - `yay -S claude-code` or whatever you prefer
3. **Describe what you want** - Plain English. Be specific about your preferences.
4. **Let AI write the configs** - It knows Hyprland syntax better than you do. Better than the person who wrote half the wiki, honestly.
5. **Iterate until perfect** - "Actually, make the gaps smaller" takes 5 seconds

No documentation rabbit holes. No Stack Overflow archaeology where every answer starts with "This question was asked 7 years ago but..." No copying someone's dotfiles and spending hours removing their anime wallpaper scripts and weird aliases.

---

## This Isn't Laziness

Some people will read this and think I'm advocating for not learning your tools. These are the same people who think suffering builds character and that you should write your own malloc before using a programming language.

Wrong.

I *understand* my Hyprland config. I read the code Claude generated. I know what `binde` vs `bind` means. I know why `wl-copy` needs `wl-paste --watch cliphist store` in the autostart.

But I didn't have to *discover* any of that through trial and error. AI gave me a working implementation, and I learned from reading correct code instead of debugging broken code written by someone who "figured it out" and never updated their blog post.

That's not laziness. That's refusing to participate in the collective hazing ritual that Linux culture mistakes for education.

---

## The Real Point

Stop using Ubuntu because it's "easier." It's not easier. It's someone else's easy. It's Canonical's idea of easy, and Canonical thinks you want to search Amazon from your app launcher.

Stop cloning dotfiles repos from GitHub users with 47 stars. You're not saving time. You're inheriting someone else's technical debt and calling it a "starter config."

Stop watching YouTube videos titled "My PERFECT Linux Setup 2026" where someone spends 40 minutes showing you their terminal color scheme. They're not teaching you anything. They're performing productivity.

Start from Arch. Start from nothing. Then tell AI exactly what you want.

You'll have a system that's:
- **Faster** - No bloat you don't need, no services you'll never use, no snap daemon eating RAM
- **Understood** - You know why everything is there because you asked for it
- **Yours** - Every keybinding, every setting, every tool chosen by you, not by a committee

4 hours and 38 minutes. That's all it took.

What's your excuse?

---

## The Proof

This blog post exists because I asked Claude to "create a resume of everything done since boot and post it to GitHub."

It read my pacman logs, checked my config files, and wrote this manifesto.

Then it created a repo and pushed it.

I didn't write a single git command. I didn't open the GitHub web interface. I didn't even open a browser.

That's the world we live in now. Keep gatekeeping Arch while the rest of us ship.

---

*Built on Arch Linux. Configured with Claude. Written at 6:00 AM because sleep is for people who need GUI installers.*

---

### What Got Installed (The Receipt)

For the skeptics who want specifics:

**Desktop:** Hyprland, Waybar, Wofi, Dunst, Hyprlock, Hypridle

**Clipboard & Screenshots:** wl-clipboard, cliphist, grim, slurp, tesseract

**Dev:** Neovim, Claude Code CLI, GitHub CLI, Rust, jq

**Terminal:** Alacritty, blesh-git, z

**Fonts:** 60+ Nerd Font variants

**Disk Tools:** gdu, disktui, diskonaut, dua-cli

---

<div align="center">

<br>

```
▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
▒                                                          ▒
▒    WHO                                                   ▒
▒        THE                                               ▒
▒            FUCK                                          ▒
▒                 AM I                                     ▒
▒                                                          ▒
▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒▒
```

<br>

**PURPLE EVERYTHING**

<br>

```
@yanbussieres
```

<sub>TESTING · ARCH · 2026</sub>

</div>
