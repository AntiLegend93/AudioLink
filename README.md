<h1 align="center">AudioLink</h1>

<p align="center"><b>Play your PC's sound through all your speakers and monitors at once, perfectly in sync.</b></p>

---

Windows normally plays sound through one device at a time. AudioLink lets your speakers, every monitor's built-in speakers, headphones, or any other output play the **same audio at the same moment**, each with its own volume, all controlled from one mixer-style window.

## Contents

- [Download and install](#download-and-install)
- [Quick start](#quick-start)
- [The window at a glance](#the-window-at-a-glance)
- [Perfect Sync](#perfect-sync)
- [Fine-tuning with TEST CLICK](#fine-tuning-with-test-click)
- [Volume tips](#volume-tips)
- [Troubleshooting](#troubleshooting)
- [FAQ](#faq)

---

## Download and install

1. Go to the [**Releases**](../../releases/latest) page.
2. Download **one** of these:
   - **AudioLink-Setup-x.y.z.exe**: the easiest option. Run it, and AudioLink appears in your Start menu with a normal uninstaller.
   - **AudioLink-x.y.z-win-x64.zip**: the portable version. Unzip it anywhere, such as your Desktop or a USB stick, and run `AudioLink.exe`.

**Requirements:** Windows 10 (version 2004 or newer) or Windows 11, 64-bit. Nothing else needs installing.

> **"Windows protected your PC"?** That message appears for apps from small developers that aren't code-signed. Click **More info → Run anyway**. You'll only see it the first time.

---

## Quick start

1. **Open AudioLink.** Your playback devices appear as strips across the window.
2. **Turn on the outputs you want:** press **ON** on each strip (A1, A2, A3...).
3. **Press START** in the top-right corner, then play some music or a video.
4. **Press PERFECT SYNC** and pick a spare device (see [Perfect Sync](#perfect-sync)). This lines up every speaker so nothing echoes.

That's it. AudioLink remembers your settings for next time.

---

## The window at a glance

### Top bar

| Button | What it does |
|---|---|
| **PERFECT SYNC** | Lines up every device, your main speakers included, so they all play at exactly the same moment. |
| **TEST CLICK** | Plays a ticking sound so you can fine-tune delays by ear. |
| **REFRESH** | Re-scans your devices. Use it after plugging something in or turning a monitor on. |
| **START / STOP** | Starts or stops AudioLink. The light next to the status text turns green while it's running. |

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
| **ON** | Sends audio to this device. |
| **Fader** | This device's volume. **0 dB** means unchanged; drag up to **+24 dB** to make it louder. **Double-click** to reset to 0. |
| **Meter** | Shows the sound level live: green is normal, yellow is loud, red is very loud. |
| **LIMIT** light | Turns orange when AudioLink is gently holding this device back to stop it distorting. |
| **DELAY** | Holds this device's sound back by a few milliseconds to line it up with the others. Perfect Sync sets this for you. |
| **DROPOUTS** | Counts tiny audio interruptions. It should stay at **0**. |
| **MUTE** | Silences just this device. |

---

## Perfect Sync

### Why you need it

Windows plays your main speakers **directly**, so they always play a few milliseconds earlier than any copy another program makes. Without Perfect Sync, your monitors would sound slightly behind your speakers, like a faint echo.

### How it works

Perfect Sync takes your main speakers off that direct path:

1. Windows sends its sound to a **spare device** that nobody listens to.
2. AudioLink picks it up and plays it on **all** your devices, main speakers included.
3. Every device then gets its own delay, so AudioLink can line them all up exactly.

### Turning it on

1. Press **PERFECT SYNC**.
2. Pick a spare device from the list. Good choices:
   - **"Digital Output"** or **"S/PDIF"**: most PCs have one, and it's usually unused.
   - An **HDMI output** with nothing plugged in.
   - The free [VB-Cable](https://vb-audio.com/Cable/) virtual device, which is made for exactly this.
3. Press **Turn on**. AudioLink switches Windows over, starts playing, and sets every delay automatically.

While Perfect Sync is on, the source fader and your keyboard's volume keys control **everything** at once.

### Turning it off

Press **PERFECT SYNC** again, press **STOP**, or simply close AudioLink. Windows switches straight back to your speakers. If AudioLink ever closes unexpectedly, it puts your speakers back the next time you open it.

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
- **LIMIT light always on?** That device is at its maximum. Turn it up at the source instead:
  - in Windows: right-click the speaker icon → **Sound settings** → choose the device → raise its volume (HDMI audio often starts at 50%);
  - on the monitor itself: its on-screen menu usually has its own volume setting.
- **Balancing:** if the monitors sound louder than your main speakers (or the reverse), use each strip's fader to even them out.

---

## Troubleshooting

| Problem | Try this |
|---|---|
| **A monitor isn't in the list** | Check it appears in Windows Sound settings. Some monitors only offer audio when their speakers are turned on in the monitor's own menu. Then press **REFRESH**. |
| **"...is locked by another program"** | Another app has taken over that device. Press Win + R → `mmsys.cpl` → right-click the device → **Properties** → **Advanced** → untick **"Allow applications to take exclusive control"** → OK. Then restart the app that was playing. |
| **Crackling or popping** | Check the **DROPOUTS** counter on that strip. If it's climbing, close heavy programs and try again. If it stays at 0, lower that strip's fader until the LIMIT light only flickers; the speaker may be pushed past what it can play cleanly. |
| **Sound echoes / devices out of sync** | Turn **PERFECT SYNC** off and on again, then fine-tune with **TEST CLICK**. |
| **A monitor goes silent when the screen sleeps** | Normal: monitors disconnect their speakers when they sleep. When it wakes, press **REFRESH**, then **START**. |
| **No sound at all after a crash** | Open AudioLink again, and it restores your speakers automatically. Or choose your speakers in Windows Sound settings. |
| **Everything is muddled up** | Reset AudioLink: close it, delete the folder `%LocalAppData%\AudioLink`, and open it again. |

---

## FAQ

**Does AudioLink change my system?**
Only while Perfect Sync is on: it switches Windows' default output to your spare device, then switches it back when you turn Perfect Sync off or close the app. Nothing is installed in the background, and no drivers are added.

**Does it add delay to my audio?**
A little, usually around a tenth of a second. It's fine for music, videos and casual gaming. For competitive gaming, you may prefer to play through one device.

**Do I need a microphone?**
No. Perfect Sync works without one.

**Can I use it with headphones or Bluetooth speakers?**
Yes. Any device Windows can play to shows up as a strip. Bluetooth adds its own noticeable delay, so use **TEST CLICK** to line it up.

**Where are my settings saved?**
In `%LocalAppData%\AudioLink\settings.json`. They're saved automatically.

**How do I uninstall?**
If you used the installer: **Settings → Apps → AudioLink → Uninstall**. If you used the zip, just delete the folder.

---

<p align="center">
  Found a bug or have an idea? <a href="../../issues">Open an issue</a>.<br/>
  Developers: see <a href="BUILDING.md">BUILDING.md</a> to build AudioLink from source.
</p>
