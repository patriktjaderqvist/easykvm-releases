# EasyKVM releases

Binaries and the auto-update feed for **[EasyKVM](https://easykvm.app)**, a software
KVM switch for macOS and Windows.

**[Download the free trial](https://easykvm.app/download.html)** ·
[How it works](https://easykvm.app/) ·
[Troubleshooting](https://easykvm.app/troubleshooting.html)

This repository holds the compiled builds and the Sparkle appcast. The source is
private. If you are looking for the product, start at
[easykvm.app](https://easykvm.app).

## What EasyKVM does

Two computers share one monitor, keyboard, mouse, and audio over the local network.
Press `Ctrl+Alt+Q` (`⌃⌥Q` on a Mac) and the monitor switches its input over DDC/CI
while the keyboard, mouse, and audio hand off to the other machine at the same time.

It is not a remote desktop tool. Nothing is streamed or compressed, because each
computer stays plugged into the monitor and keeps driving it natively, so you keep
full resolution, refresh rate, and HDR.

- macOS 13+ and Windows 10/11, one licence covers both for a single user
- Monitor input switching over DDC/CI, on one monitor or several
- Keyboard, mouse, bidirectional audio, and a shared clipboard
- LAN only. Nothing but the licence check ever reaches the internet
- No analytics and no telemetry
- $29.99 one time, with a 3-day trial that does not ask for a card

Automatic monitor switching is driven by a Windows machine in the pair, so Mac plus
PC and PC plus PC swap the monitor on their own. Two Macs share keyboard, mouse,
audio, and clipboard, and you switch the monitor input yourself.

## Installing

Grab the latest build from [Releases](../../releases/latest).

EasyKVM is in beta and the builds are not code-signed yet, so the first launch needs
one extra click:

- **macOS**: right-click the app and choose Open rather than double-clicking it.
- **Windows**: SmartScreen shows "Windows protected your PC". Choose More info, then
  Run anyway.

After that both platforms update themselves in place. There is an opt-in beta channel
in the app's settings if you want builds before they reach stable.

## Does my monitor work?

Input switching uses DDC/CI, which most monitors made after roughly 2015 support. Two
things trip people up more often than anything else:

1. **DDC/CI is usually off by default.** Turn it on in the monitor's own on-screen
   menu. On some panels it switches itself back off after the monitor loses power.
2. **Most panels only accept DDC/CI from the input currently on screen.** Switching
   away works because the machine sending the command is the one being displayed.
   Switching back is the hard direction, and EasyKVM handles it by asking the computer
   that is on screen to do the switch.

Some MSI monitors built on MStar scalers advertise the standard input codes and then
use a private numbering internally, so standard commands are acknowledged and quietly
ignored. EasyKVM detects that and translates automatically.

If your monitor will not cooperate, keyboard, mouse, audio, and clipboard still move
on the hotkey and you switch the screen with the monitor's own button. There is a
3-day trial and a 14-day refund, so you can find out before paying.

More detail: [Troubleshooting](https://easykvm.app/troubleshooting.html) ·
[How DDC/CI input switching works](https://easykvm.app/switch-monitor-input-with-keyboard-shortcut.html)

## Compared to other tools

Synergy, Barrier, Input Leap, Deskflow, ShareMouse, Logitech Flow, and Mouse Without
Borders share a keyboard and mouse between computers that each keep their own screen,
and you cross between them by moving the pointer to the screen edge. EasyKVM is built
for one shared monitor and switches the monitor's physical input as part of the same
hotkey.

[Synergy](https://easykvm.app/synergy-alternative.html) ·
[Barrier / Input Leap](https://easykvm.app/barrier-alternative.html) ·
[Deskflow](https://easykvm.app/deskflow-alternative.html) ·
[ShareMouse](https://easykvm.app/sharemouse-alternative.html) ·
[Logitech Flow](https://easykvm.app/logitech-flow-alternative.html) ·
[Mouse Without Borders](https://easykvm.app/mouse-without-borders-alternative.html) ·
[Multiplicity](https://easykvm.app/multiplicity-alternative.html) ·
[vs a hardware KVM switch](https://easykvm.app/kvm-switch-for-two-computers.html) ·
[vs remote desktop](https://easykvm.app/kvm-vs-remote-desktop.html)

## Support

[Contact form](https://easykvm.app/contact.html) or support@avendavi.com.
Issues are not tracked here, since this repository only carries the builds.

An [Avendavi](https://avendavi.com) product, made in Sweden.
