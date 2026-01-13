# Start From Scratch. Use Arch. Let AI Do The Heavy Lifting.

*A manifesto for the impatient developer who refuses to compromise*

---

## The Conventional Wisdom Is Wrong

Everyone tells you the same thing: "Just use Ubuntu. Use a preconfigured dotfiles repo. Don't waste time on setup."

Bullshit.

That advice made sense in 2015. It's catastrophically wrong in 2026.

Here's what I did this morning: I booted a fresh Arch Linux install at 1:21 AM. By 6:00 AM, I had a fully configured Hyprland desktop with vim-style keybindings, 60+ development fonts, a screenshot tool with live OCR, clipboard history, auto-lock, Neovim with LSP, and every dev tool I need.

**4 hours and 38 minutes.** From nothing to a development environment that's *exactly* what I want.

Not someone else's dotfiles. Not Ubuntu's idea of sensible defaults. *Mine.*

---

## What Actually Got Done

Let me be concrete. This isn't hypothetical productivity porn:

- **Full Hyprland Wayland Compositor** - Configured from scratch with waybar, wofi, dunst
- **60+ Nerd Fonts** - FiraCode, JetBrains Mono, Cascadia Code, Iosevka, you name it
- **Vim-style Everything** - HJKL for window focus, move, resize. No arrow keys needed.
- **macOS-style Screenshots with OCR** - `Super+Shift+6` selects a region and extracts text. In 2026. On Linux.
- **Clipboard History** - `Super+V` brings up a searchable history. Obviously.
- **Power Management** - Auto-lock at 5 min, screen off at 10 min, proper sleep handling
- **Neovim** - LSP, completion, telescope, the works
- **Claude Code CLI** - AI pair programmer in the terminal
- **GitHub CLI** - SSH auth, ready to ship

Ten significant accomplishments. Not "I installed VS Code and changed the theme."

---

## The Secret: AI Changed Everything

Here's why the old advice is wrong: **AI assistants are absurdly good at system configuration now.**

I didn't memorize Hyprland syntax. I didn't dig through wiki pages for hypridle timeout settings. I didn't debug why my screenshot script wasn't working with Wayland's clipboard.

I described what I wanted. Claude figured out the implementation.

```
"Add vim-style HJKL keybindings for moving windows"
"Make Super+Shift+6 select a region and OCR the text to clipboard"
"Configure hypridle to lock at 5 minutes and screen off at 10"
```

Three sentences. Three features. Done correctly the first time.

---

## Why Arch Specifically?

Because Arch gives you nothing. And that's the point.

Ubuntu gives you someone else's opinions pre-installed. Pop!_OS gives you System76's workflow assumptions. Even Fedora comes with decisions already made.

Arch gives you a blank canvas. You install exactly what you need. Nothing you don't.

When you combine that clean slate with an AI that can implement whatever you describe, you get something unprecedented: **a truly custom system built in hours instead of weeks.**

The old tradeoff was:
- Custom = slow and painful
- Fast = accept someone else's defaults

That tradeoff is dead. Custom AND fast is now possible.

---

## The Workflow

Here's how it actually works:

1. **Install Arch** - Use `archinstall`, takes 10 minutes
2. **Install your AI tool** - `yay -S claude-code` or whatever you prefer
3. **Describe what you want** - Plain English. Be specific about your preferences.
4. **Let AI write the configs** - It knows Hyprland syntax better than you do
5. **Iterate until perfect** - "Actually, make the gaps smaller" takes 5 seconds

No documentation rabbit holes. No Stack Overflow archaeology. No copying someone's dotfiles and spending hours removing the stuff you don't want.

---

## This Isn't Laziness

Some people will read this and think I'm advocating for not learning your tools.

Wrong.

I *understand* my Hyprland config. I read the code Claude generated. I know what `binde` vs `bind` means. I know why `wl-copy` needs `wl-paste --watch cliphist store` in the autostart.

But I didn't have to *discover* any of that through trial and error. AI gave me a working implementation, and I learned from reading correct code instead of debugging broken code.

That's not laziness. That's efficiency.

---

## The Real Point

Stop using Ubuntu because it's "easier." It's not easier. It's someone else's easy.

Stop cloning dotfiles repos and spending hours customizing someone else's config. You're not saving time. You're just shifting when you spend it.

Start from Arch. Start from nothing. Then tell AI exactly what you want.

You'll have a system that's:
- **Faster** - No bloat you don't need
- **Understood** - You know why everything is there
- **Yours** - Every keybinding, every setting, every tool

4 hours and 38 minutes. That's all it took.

---

## The Proof

This blog post exists because I asked Claude to "create a resume of everything done since boot and post it to GitHub."

It read my pacman logs, checked my config files, and wrote this manifesto.

Then it created a repo and pushed it.

That's the world we live in now. Act accordingly.

---

*Built on Arch Linux. Configured with Claude. Written at 6:00 AM because sleep is for people who use Ubuntu.*

---

### What Got Installed (The Receipt)

For the skeptics who want specifics, here's the pacman log from this session:

**Desktop Environment:**
- Hyprland (Wayland compositor)
- Waybar (status bar)
- Wofi (application launcher)
- Dunst (notifications)
- Hyprlock + Hypridle (screen lock and power management)

**Clipboard & Screenshots:**
- wl-clipboard
- cliphist
- grim + slurp
- tesseract + tesseract-data-eng (OCR)

**Development:**
- Neovim
- Claude Code CLI
- GitHub CLI
- Rust toolchain
- jq

**Terminal & Shell:**
- Alacritty
- blesh-git (bash enhancements)
- z (directory jumping)

**Fonts:**
- 60+ Nerd Font variants (the entire nerd-fonts package)

**Disk Analysis:**
- gdu
- disktui
- diskonaut
- dua-cli

That's a complete development environment. In one morning. On Arch. With AI.

No excuses left.
