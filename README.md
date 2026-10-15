<p align="center">
  <img src="docs/logo.png" width="120" alt="AudioLink logo" />
</p>

<h1 align="center">AudioLink</h1>

<p align="center"><b>Play your PC's sound through all your speakers and monitors at once, perfectly in sync.</b></p>

<p align="center">
  <a href="../../releases/latest"><img src="docs/download.png" height="32" alt="Download" /></a>
  &nbsp;
  <a href="https://venmo.com/code?user_id=3587678062773330218&created=1791519560"><img src="docs/donate.png" height="32" alt="Donate with Venmo" /></a>
</p>

---

Windows normally plays sound through one device at a time. AudioLink lets your speakers, every monitor's built-in speakers, headphones, Bluetooth speakers, or any other output play the **same audio at the same moment**, each with its own volume, all controlled from one mixer-style window.

## Features

- **Play everywhere at once:** speakers, monitor speakers, headphones and Bluetooth, all together.
- **Perfect Sync:** lines up every device so nothing echoes. No microphone needed.
- **A real mixer:** volume (up to +24 dB), live meters, delay, mute, bass and treble for every device, plus a master fader.
- **Stereo across your desk:** set each device to Stereo, Mono, Left only, Right only or Swap.
- **App routing:** choose which device each app plays on.
- **Profiles:** save setups like "Movie" or "Gaming" and switch in one click.
- **Runs in the background:** lives in the system tray, starts with Windows, and reconnects devices by itself.
- **Keeps itself up to date:** new versions install in a few seconds.
- **Looks after itself:** if the sound ever stops, AudioLink notices and gets it going again on its own.

## Contents

- [Download and install](#download-and-install)
- [Quick start](#quick-start)
- [The window at a glance](#the-window-at-a-glance)
- [Perfect Sync](#perfect-sync)
- [Fine-tuning with TEST CLICK](#fine-tuning-with-test-click)
- [Volume tips](#volume-tips)
- [Updates](#updates)
- [Troubleshooting](#troubleshooting)
- [FAQ](#faq)
- [Support AudioLink](#support-audiolink)

---

## Download and install

1. Go to the [**Releases**](../../releases/latest) page.
2. Download **AudioLink-Setup-x.y.z.exe** and run it. AudioLink appears in your Start menu, with an optional desktop shortcut and a normal uninstaller. It installs just for you, so it doesn't need admin rights, and it **updates itself**.

**Requirements:** Windows 10 (version 2004 or newer) or Windows 11, 64-bit. Nothing else needs installing.

> **"Windows protected your PC"?** That message appears for apps from small developers that aren't code-signed. Click **More info → Run anyway**. You'll only see it the first time.

---

## Quick start

1. **Open AudioLink.** Your playback devices appear as strips across the window.
2. **Turn on the outputs you want:** press **ON** on each strip (A1, A2, A3...).
3. **Press START** in the top-right corner, then play some music or a video.
4. **Press PERFECT SYNC** (see [Perfect Sync](#perfect-sync)). This lines up every speaker so nothing echoes.

That's it. AudioLink remembers your settings (and where you put the window) for next time. Closing the window keeps it running in the system tray by the clock.

---

## The window at a glance

### Top bar

| Button | What it does |
|---|---|
| **♥ DONATE** | Support AudioLink on Venmo, if you'd like to. |
| **PROFILES** | Save your setup (e.g. "Movie", "Gaming", "Headphones only") and switch between them with one click. |
| **APPS** | Choose which device each app plays on, e.g. Spotify on the monitors only, a game on headphones only. |
| **PERFECT SYNC** | Lines up every device, your main speakers included, so they all play at exactly the same moment. |
| **TEST CLICK** | Plays a ticking sound so you can fine-tune delays by ear. |
| **REFRESH** | Re-scans your devices. Use it after plugging something in or turning a monitor on. |
| **⚙ Settings** | **Start with Windows**, **Keep running in the tray when closed**, the **Bluetooth delay preset**, the **Perfect Sync device**, **Copy diagnostics** and **Open log folder** (for reporting a problem), **update** options, and **Exit**. |
| **START / STOP** | Starts or stops AudioLink. The status light (above the strips) turns green while it's running. |

### Source strip (left)

The **SOURCE** is the device Windows normally plays to, usually your main speakers. AudioLink copies everything playing there to your other devices.

- **Device picker:** choose which device is the source.
- **Fader:** your speakers' volume. It's the same setting as the Windows volume slider, but it doesn't change the other outputs.
- **MUTE:** silences the source speakers only. Everything else keeps playing.
- **OUTPUTS FOLLOW:** turn it on to make the source fader a *master volume* that turns everything up and down together.

### Output strips (A1, A2, A3...)

Each of your other devices gets its own strip:

| Control | What it does |
|---|---|
| **Name** | Click it to give the strip your own name, like "Left monitor". |
| **BT** badge | Marks a Bluetooth device. Perfect Sync automatically allows for Bluetooth's extra delay. |
| **ON** | Sends audio to this device. |
| **FX** | **Channels** (Stereo, Mono, Left only, Right only, Swap) and **Bass / Treble**. Tip: Left only on your left monitor and Right only on your right one gives real stereo across your desk. |
| **Fader** | This device's volume. **0 dB** means unchanged; drag up to **+24 dB** to make it louder. **Double-click** to reset to 0. |
| **Meter** | Shows the sound level live: green is normal, yellow is loud, red is very loud. |
| **LIMIT** light | Turns orange when AudioLink is gently holding this device back to stop it distorting. |
| **DELAY** | Holds this device's sound back by a few milliseconds to line it up with the others. Perfect Sync sets this for you. |
| **DROPOUTS** | Counts tiny audio interruptions. It should stay at **0**. |
| **MUTE** | Silences just this device. |

### Master strip (right)

One **fader** that turns every output up or down together (up to +12 dB), a meter showing the loudest output, and **MUTE ALL**.

### System tray

Closing the window keeps AudioLink running next to the clock. **Click** the tray icon to open the window again; **right-click** it for Start/Stop, Perfect Sync, Mute all, your profiles, updates, and **Exit**. Turn this off under ⚙ Settings if you'd rather closing the window quit AudioLink.

With **Start with Windows** on, AudioLink starts quietly in the tray when you sign in and carries on where you left off, Perfect Sync included.

### Automatic reconnect

When a monitor wakes up, Bluetooth reconnects, or you plug a device back in, AudioLink notices and switches its strip back on by itself. If Windows changes its default output while Perfect Sync is on (which it does when new devices appear), AudioLink switches it straight back. And if the sound ever stops reaching AudioLink, it restarts itself within a few seconds.

---

## Perfect Sync

### Why you need it

Windows plays your main speakers **directly**, so they always play a few milliseconds earlier than any copy another program makes. Without Perfect Sync, your monitors would sound slightly behind your speakers, like a faint echo.

### How it works

Perfect Sync takes your main speakers off that direct path:

1. Windows sends its sound to a **spare device** that nobody listens to. AudioLink keeps that device awake, so it can't switch itself off when things go quiet.
2. AudioLink picks it up and plays it on **all** your devices, main speakers included.
3. Every device then gets its own delay, so AudioLink can line them all up exactly. Bluetooth devices automatically get extra time for their wireless delay.

### Turning it on

Press **PERFECT SYNC**. That's it: AudioLink picks a spare device by itself, switches Windows over, starts playing, and sets every delay automatically. A message tells you which device it chose.

It prefers devices nobody can hear: the free [VB-Cable](https://vb-audio.com/Cable/) virtual device if you have it, then a **"Digital Output"** / **S/PDIF**, then any other unused output. It never picks headphones or Bluetooth.

**Want a different one?** If you can ever hear sound coming straight from the spare device, choose another under **⚙ Settings → Perfect Sync device…**.

While Perfect Sync is on, the source fader and your keyboard's volume keys control **everything** at once.

### Turning it off

Press **PERFECT SYNC** again, press **STOP**, or exit AudioLink. Windows switches straight back to your speakers. If AudioLink ever closes unexpectedly, it puts your speakers back the next time you open it.

### "No spare device"?

Most PCs have one hidden:

1. Press **Win + R**, type `mmsys.cpl`, and press Enter.
2. Right-click in the empty space of the list and tick **Show Disabled Devices**.
3. Right-click a greyed-out output (often "Digital Output") and choose **Enable**.
4. Back in AudioLink, press **REFRESH**, then **PERFECT SYNC**.

No hidden device either? Install [VB-Cable](https://vb-audio.com/Cable/). It's free and adds a silent device that works perfectly.

---

## Fine-tuning with TEST CLICK

Some monitors add a little delay inside their own electronics, and no software can see that. If something still sounds slightly "doubled":

1. Press **TEST CLICK**. A tick plays about once a second through every device.
2. Listen. If the ticks sound like a **double "tick-tick"** instead of one sharp click, a device is ahead of the others.
3. Slowly raise that device's **DELAY** slider until all the ticks land together as one click.
4. Press **TEST CLICK** again to stop.

---

## Volume tips

- **Louder:** raise the strip's fader above 0 dB, up to +24 dB.
- **Everything at once:** use the **MASTER** fader on the right.
- **LIMIT light always on?** That device is at its maximum. Turn it up at the source instead:
  - in Windows: right-click the speaker icon → **Sound settings** → choose the device → raise its volume (HDMI audio often starts at 50%);
  - on the monitor itself: its on-screen menu usually has its own volume setting.
- **Thin-sounding monitor speakers?** Open the strip's **FX** and raise the **Bass**.
- **Balancing:** if the monitors sound louder than your main speakers (or the reverse), use each strip's fader to even them out.

---

## Updates

AudioLink checks for a new version every time it starts, and every few hours while it's running in the tray. When one is out, a green bar appears at the bottom of the window (it closes itself after 5 minutes). Click **Update now**: AudioLink downloads the update, installs it, and reopens in a few seconds, keeping all your settings. The first time you open a new version, a short **"What's new"** message shows what changed.

You can also update from the tray icon's right-click menu, check by hand under **⚙ Settings → Check for updates**, or turn automatic checks off there.

---

## Troubleshooting

| Problem | Try this |
|---|---|
| **A monitor isn't in the list** | Check it appears in Windows Sound settings. Some monitors only offer audio when their speakers are turned on in the monitor's own menu. Then press **REFRESH**. |
| **"...is locked by another program"** | Another app has taken over that device. Press Win + R → `mmsys.cpl` → right-click the device → **Properties** → **Advanced** → untick **"Allow applications to take exclusive control"** → OK. Then restart the app that was playing. |
| **Crackling or popping** | Check the **DROPOUTS** counter on that strip. If it's climbing, close heavy programs and try again. If it stays at 0, lower that strip's fader until the LIMIT light only flickers; the speaker may be pushed past what it can play cleanly. |
| **Sound echoes / devices out of sync** | Turn **PERFECT SYNC** off and on again, then fine-tune with **TEST CLICK**. |
| **An app won't move to another device** | Pause and play it again; some apps only switch then. Or use Windows' own setting: **APPS → Open Windows' per-app sound settings**. |
| **No sound at all after a crash** | Open AudioLink again, and it restores your speakers automatically. Or choose your speakers in Windows Sound settings. |
| **Something else is wrong** | Open **⚙ Settings → Copy diagnostics** and paste the result into an [issue](../../issues). It lists your devices and what AudioLink has been doing, which usually shows exactly what happened. |
| **Everything is muddled up** | Reset AudioLink: exit it, delete the folder `%LocalAppData%\AudioLink`, and open it again. |

---

## FAQ

**Does AudioLink change my system?**
Only while Perfect Sync is on: it switches Windows' default output to your spare device, then switches it back when you turn Perfect Sync off or exit the app. No drivers are added.

**Does it add delay to my audio?**
A little, usually around a tenth of a second (more with Bluetooth). It's fine for music, videos and casual gaming. For competitive gaming, you may prefer to play through one device.

**Do I need a microphone?**
No. Perfect Sync works without one.

**Can I use it with headphones or Bluetooth speakers?**
Yes. Any device Windows can play to shows up as a strip. Bluetooth devices get a **BT** badge, and Perfect Sync automatically adds the **Bluetooth delay preset** (150 ms, adjustable under ⚙ Settings). Fine-tune with **TEST CLICK** if needed.

**How does app routing work?**
**APPS** lists the apps currently making sound. Pick a device for an app and it plays *only* there, directly. Choose "Everywhere" to put it back in the AudioLink mix. It's the same setting as Windows' own per-app sound settings, so Windows remembers it.

**How do I close AudioLink completely?**
Right-click the tray icon → **Exit AudioLink**, or use **⚙ Settings → Exit AudioLink**.

**Where are my settings saved?**
In `%LocalAppData%\AudioLink\settings.json`. They're saved automatically.

**How do I uninstall?**
**Settings → Apps → AudioLink → Uninstall**. It closes AudioLink, switches Windows back to your speakers if Perfect Sync was on, and turns off Start with Windows. Your settings stay in `%LocalAppData%\AudioLink` in case you reinstall; delete that folder too if you want them gone.

---

## Support AudioLink

AudioLink is free. If it's useful to you, you can buy me a coffee:

**[Donate with Venmo](https://venmo.com/code?user_id=3587678062773330218&created=1791519560)**

Thank you!

---

<p align="center">
  Found a bug or have an idea? <a href="../../issues">Open an issue</a>.
</p>
