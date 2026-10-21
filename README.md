# N.O.M.A.D Desktop

**Review and compare your N.O.M.A.D trips on a Windows PC.**

N.O.M.A.D Desktop is the companion to the N.O.M.A.D phone app. Get your
trips off the phone, then on a big screen:

- browse every trip: map, speed and acceleration charts, segments, signal
  delays and congestion, harsh braking, and the time-distance diagram
- **compare** trips on the same route (up to 32 at once), section by section,
  to see exactly where one run was faster or slower than another, over the
  whole route or any stretch of it
- **find every trip that drove a stretch of road** in the same direction,
  wherever it started or finished, for route audits
- organise trips into **project libraries**, for example one per route audit:
  new trips arrive in *Imported*, and you move them into the right library
- export trips and comparisons to CSV, Excel or GPX

It doesn't record trips. Recording stays on the phone.

**New to it?** The [user guide](USER_GUIDE.md) walks through every page, and
is updated with every version.

## Download

**[Download the latest version](https://github.com/nomadtrafficapp-ship-it/nomad-desktop-releases/releases/latest/download/nomad-desktop-setup.exe)**:
`nomad-desktop-setup.exe`, which is always the newest version. The short
link to share is **nomadtrafficapp-ship-it.github.io/desktop**.

Every release is also listed on the
[releases page](https://github.com/nomadtrafficapp-ship-it/nomad-desktop-releases/releases),
with notes and checksums.

You need **Windows 10 or 11, 64-bit**.

## Install

1. Run the downloaded `setup.exe`.
2. Windows may show **"Windows protected your PC"**. This appears because
   the installer isn't code-signed. Click **More info**, then **Run anyway**.
3. Follow the installer. It installs just for you and doesn't need
   administrator rights. You'll find N.O.M.A.D Desktop in the Start menu.

## Get your trips onto the PC

**Straight from the phone (recommended).** On the PC, open **Receive**. On the
phone, open **Export → Send to desktop** (in **Settings** on phone app 1.5.1
and earlier), choose your PC, and type the pairing code the PC shows.
- **Wi-Fi:** the phone and PC must be on the same network. The first time,
  Windows may ask whether to allow N.O.M.A.D Desktop on the network; allow
  it on **private** networks.
- **USB cable:** plug the phone in, choose **File transfer** in the
  phone's USB notification, and choose **USB cable** on the phone. This
  works anywhere in the app, not only on Receive. The PC picks the trips
  up, checks them and asks before importing, then removes them from the
  phone. It needs desktop 0.3.1 and phone app 1.5.1 or later.

Send to desktop needs a version of the phone app that has it. With an older
phone app, use the next option.

**Or from an exported file.** On the phone, use **Export → Export database**
(in **Settings** on phone app 1.5.1 and earlier) and copy the `.sqlite` file
from the phone's `Downloads/Nomad` folder to the PC. In the desktop app, click **Import database**.

## Your data

- Your trips stay on your PC, in
  `%APPDATA%\com.nomad\N.O.M.A.D Desktop`. Nothing is uploaded anywhere.
- Like the phone app, it looks up map tiles and road details from
  OpenStreetMap services (OpenStreetMap, OSRM, Overpass).
- To look for updates it asks GitHub for the latest release, at most twice
  a day (you can turn this off in About). Nothing about you or your trips
  is sent.
- Over Wi-Fi, the PC only accepts trips while the
  **Receive** page is open, and only from a phone that has entered the
  pairing code shown on screen. Use Wi-Fi on networks you trust, such as
  home or your phone's hotspot.
- With a phone plugged in on **File transfer**, the app looks only in the
  phone's `Download/Nomad/Desktop` folder, asks before importing what it
  finds there, and removes it from the phone after importing.
- Importing adds new trips to the *Imported* library. Trips already on the
  PC are kept as they are, names and libraries included. The library is
  backed up before each import, in the `backups` folder inside the data
  folder.

The full details are in the
[privacy policy](https://nomadtrafficapp-ship-it.github.io/nomad-privacy-policy/#desktop).

## Update

From version 0.2.2 the app **updates itself**. When a new version is out,
a bar at the top of the window offers it. Click **Update now** and the app
downloads it, checks it against its published checksum, then closes,
installs and reopens. Your trips are kept. You can also check from
**About → Check for updates**, and turn automatic checks off there.

On **0.2.1**, download and run the new `setup.exe` once. It upgrades the
installed copy, keeps your trips, and later updates arrive automatically.

## Uninstall

Go to **Settings → Apps → Installed apps → N.O.M.A.D Desktop → Uninstall**.
Your trips are left in `%APPDATA%\com.nomad\N.O.M.A.D Desktop`; delete that
folder to remove them too.

## Check your download

Each release lists the installer's SHA-256 checksum. In PowerShell, run:

```
Get-FileHash .\nomad_desktop-<version>-setup.exe -Algorithm SHA256
```
