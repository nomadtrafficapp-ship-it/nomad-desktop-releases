# N.O.M.A.D Desktop

**Review and compare your N.O.M.A.D trips on a Windows PC.**

N.O.M.A.D Desktop is the companion to the N.O.M.A.D phone app. Get your
trips off the phone, then on a big screen:

- browse every trip: map, speed and acceleration charts, segments, signal
  delays and congestion, harsh braking, and the time-distance diagram
- **compare** trips on the same route (up to 8 at once), section by section,
  to see exactly where one run was faster or slower than another, over the
  whole route or any stretch of it
- export trips and comparisons to CSV, Excel or GPX

It doesn't record trips. Recording stays on the phone.

## Download

**[Download the latest version](https://github.com/nomadtrafficapp-ship-it/nomad-desktop-releases/releases/latest)**.
On that page, under *Assets*, choose `nomad_desktop-<version>-setup.exe`.

You need **Windows 10 or 11, 64-bit**.

## Install

1. Run the downloaded `setup.exe`.
2. Windows may show **"Windows protected your PC"**. This appears because
   the installer isn't code-signed. Click **More info**, then **Run anyway**.
3. Follow the installer. It installs just for you and doesn't need
   administrator rights. You'll find N.O.M.A.D Desktop in the Start menu.

## Get your trips onto the PC

**Straight from the phone (recommended).** On the PC, open **Receive**. On the
phone, open **Settings → Send to desktop**, choose your PC, and type the
pairing code the PC shows.
- **Wi-Fi:** the phone and PC must be on the same network. The first time,
  Windows may ask whether to allow N.O.M.A.D Desktop on the network; allow
  it on **private** networks.
- **USB cable:** connect the phone with USB debugging turned on (Android
  Developer options). The PC also needs Android's platform-tools (`adb`)
  installed.

Send to desktop needs a version of the phone app that has it. With an older
phone app, use the next option.

**Or from an exported file.** On the phone, use **Settings → Export
database** and copy the `.sqlite` file from the phone's `Downloads/Nomad`
folder to the PC. In the desktop app, click **Import database**.

## Your data

- Your trips stay on your PC, in
  `%APPDATA%\com.nomad\N.O.M.A.D Desktop`. Nothing is uploaded anywhere.
- Like the phone app, it looks up map tiles and road details from
  OpenStreetMap services (OpenStreetMap, OSRM, Overpass).
- The PC only accepts trips while the **Receive** page is open, and only
  from a phone that has entered the pairing code shown on screen. Use it on
  networks you trust, such as home or your phone's hotspot.
- Importing replaces the trips loaded on the PC. The previous set is kept
  in the `backups` folder inside the data folder.

## Update

Download and run the new `setup.exe`. It upgrades the installed copy and
keeps your trips.

## Uninstall

Go to **Settings → Apps → Installed apps → N.O.M.A.D Desktop → Uninstall**.
Your trips are left in `%APPDATA%\com.nomad\N.O.M.A.D Desktop`; delete that
folder to remove them too.

## Check your download

Each release lists the installer's SHA-256 checksum. In PowerShell, run:

```
Get-FileHash .\nomad_desktop-<version>-setup.exe -Algorithm SHA256
```
