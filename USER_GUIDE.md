# N.O.M.A.D Desktop user guide

This guide is for **N.O.M.A.D Desktop 0.5.4**. In the app, **About** shows
which version you have.

N.O.M.A.D Desktop is the Windows companion to the N.O.M.A.D phone app. The
phone records trips; the desktop is where you review them on a large screen,
organise them into project libraries, and compare repeated runs of the same
route section by section. It does not record trips itself.

- [Getting started](#getting-started)
- [The window](#the-window)
- [Getting trips from the phone](#getting-trips-from-the-phone)
- [Trips](#trips)
- [Compare](#compare)
- [Settings](#settings)
- [About and updates](#about-and-updates)
- [Arranging the window](#arranging-the-window)
- [Glossary](#glossary)
- [Troubleshooting](#troubleshooting)

---

## Getting started

1. **Install.** Download `nomad-desktop-setup.exe` from
   [nomadtrafficapp-ship-it.github.io/desktop](https://nomadtrafficapp-ship-it.github.io/desktop)
   and run it. If Windows shows *Windows protected your PC*, choose
   **More info → Run anyway** (the installer isn't code-signed). It installs
   for your Windows account only and needs no administrator rights.
2. **Get your trips onto the PC.** Either send them from the phone (see
   [Getting trips from the phone](#getting-trips-from-the-phone)) or import
   an exported database file with **Import database…**.
3. **Review and compare.** Open a trip on the **Trips** page; tick several
   runs of the same route and click **Compare**.

Your trips stay on this PC. Changes made here — renames, libraries,
deletions — never affect the phone.

## The window

- **Navigation rail** (left): **Trips**, **Compare**, **Receive**,
  **Settings** and **About**. The button at the bottom of the rail imports a
  database file.
- **Status bar** (bottom): how many trips and libraries are loaded and when
  the last import was.
- **Update bar** (top, only when one is available): a newer version is ready
  to install. See [About and updates](#about-and-updates).

The window can't be made smaller than about 1024 × 700, so every page keeps
room for its content.

## Getting trips from the phone

There are four ways. Each import **adds** new trips to the *Imported*
library; trips already on the PC keep their names and libraries, and trips
you deleted here aren't brought back. The library is backed up before every
import.

### USB cable, File transfer (recommended)

No setup needed on the phone.

1. Plug the phone in and choose **File transfer** in its USB notification.
2. On the phone: **Export → Send to desktop → USB cable**.
3. The desktop picks the trips up — on any page — and asks before importing
   them. Choose **Import**, or **Not now** to leave them for later (they stay
   listed on the **Receive** page).

### Wi-Fi

1. Open the **Receive** page. It listens only while it is open and shows a
   six-digit **pairing code**.
2. On the phone, on the same network: **Export → Send to desktop**, choose
   this computer (or enter one of the addresses the page lists), and enter the
   code. Each code works once.
3. The desktop checks what arrived and asks before importing it.

If Windows asks whether to allow N.O.M.A.D Desktop on the network, allow it
on **private** networks.

### USB cable with USB debugging

For phones with Developer options' USB debugging turned on, and a PC with
Android platform-tools (adb) installed. Keep the **Receive** page open, plug
the phone in, and on the phone choose **USB cable with USB debugging**.

### A database file

On the phone, **Export → Export database** saves a `.sqlite` file. Copy it to
the PC and use **Import database…** (rail button, **Settings**, or the welcome
screen). Bluetooth works this way too: share the file from the phone and
receive it with Windows *Receive files*.

## Trips

Three panes, left to right: libraries, the trip list, and the selected trip.

### Libraries

- **All trips** shows everything; **Imported** is where new trips land.
- **New library** (folder button): create a library for a project, a route or
  a client.
- **Move trips** by dragging them from the list onto a library, or with a
  trip's **Move to library…**. Each trip is in one library.
- A library's **⋮** menu renames or deletes it. Deleting a library moves its
  trips back to *Imported*; it doesn't delete them.
- The **‹** button folds the pane to a slim strip. On a narrow window it folds
  away by itself to keep room for the trip's details.

### The trip list

- **Search** by name, date or road.
- **Journey** narrows the list to repeated trips that start and finish in the
  same places.
- **Sort** (≡ button): newest, oldest, shortest or longest time, longest
  distance.
- **⋮** (next to Sort): move every trip currently shown to a library.
- Each row shows the trip's name or date, distance, duration, library (in
  *All trips*) and its start and end roads.
- **Tick box**: adds the trip to the comparison; the coloured bar beside it is
  its colour on the Compare page, and a ★ marks the baseline. The bar above
  the list counts the ticked trips (up to 32) and has **Clear** and
  **Compare**.
- A row's **⋮** menu:
  - **Rename…**
  - **Move to library…**
  - **Compare with same journey…** — opens Compare with this trip and its
    repeats.
  - **Find trips on part of this route…** — opens Compare with this trip, so
    you can pick a stretch and find every other trip that drove it.
  - **Delete trip** (from this PC only).

### The selected trip

Click a trip to open its details, the same screen as on the phone:

- a summary (distance, speeds, acceleration, moving and stopped time, time in
  congestion);
- the **route map**, with a playback slider;
- **Speed over time** and **Acceleration over time** charts;
- **Segments** — the trip split into moving and stopped parts, with roads,
  cross streets, signals and speed limits;
- **Congestion episodes** — stop-start queues, with HCM-style control delay
  and level of service;
- **Harsh braking / acceleration events**.

The toolbar renames the trip, opens its **time-distance diagram**, re-checks
its details, and exports it (**CSV, XLSX and GPX** to a folder you choose).

Opening a trip looks up any details still missing — road names, cross
streets, signals — online, the same way the phone does.

## Compare

Compare puts up to 32 trips of the same route side by side, measured against
a **baseline** trip. Add trips by ticking them on the **Trips** page, by
**Compare with same journey…**, or with **Find trips on this stretch…**.

### Choosing what to compare

- **Trip chips** across the top: click one to make it the baseline (★); its
  **×** removes it. **Add trips** goes back to the Trips page.
- **Suggest baseline** picks the trip whose route the others share most.
- **Clear all** empties the comparison to start a new one (**Undo** in the
  message brings it back).
- **Export CSV…** saves every table and figure below.
- **Time sections between** sets the checkpoints the route is timed between:
  - **Signals** — the baseline's traffic signals;
  - **Intersections** — every cross street;
  - **Fixed distance** — every 250 m, 500 m, 1 km or 2 km.
  
  **Include pedestrian crossings** adds crossings as checkpoints; it is on by
  default.

### Comparing a stretch

By default every figure covers the **common span**: from the first to the
last checkpoint every trip passed. To measure part of the route only:

- pick a start and end checkpoint in **Compare from … to …**; or
- click a numbered checkpoint on the map and choose **Start stretch here** or
  **End stretch here**.

**Whole common span** goes back to the full route. The page stays where it is
on screen while you pick.

**Find trips on this stretch…** lists every trip in the library (or in one
library — **Search in**) that drove the stretch end to end in the same
direction, wherever it started or finished. A trip counts when it passed
within 35 m of at least 90% of the stretch, heading the same way, in order,
and was on it at both ends. Tick the ones you want and **Add to comparison**,
or **Move to library…** to collect them for a route study.

Notes above the summary list any trip that didn't drive the compared span
(left off the charts) or took a different road for part of it (its time is
then an end-to-end time, not one over the same road).

### Summary

One row per trip: departure time, time over the span (with its difference
from the baseline), time stopped and stops in the span, whole-trip time,
distance, average speed, time in congestion and control delay. Longer names
are shortened; hover for the full name. Wide tables scroll sideways — use the
scrollbar under them.

### Time-distance

Each trip's progress along the route over time: steeper lines are slower,
flat runs are stops. Vertical lines mark the checkpoints, named above the
chart with their number (as on the map and in the tables), signal or crossing
and cross street.

**Line up trips on** sets each trip's 0:00:

- **Moving off at checkpoint N** — when the trip moved off from its last stop
  before the first signal of the stretch, about when that signal turned green
  for it. The lines then show when each trip reached the signals after it —
  use this to study **signal coordination**. The approach and the wait in the
  queue appear below zero. Trips that didn't stop there are timed from the
  start of the diagram instead; the chart's description names them.
- **Passing through checkpoint N** — when each trip crossed that first
  intersection, stopped there or not.
- **Back of the queue** — where each trip passed the start of the diagram, so
  the time spent queueing shows on each line.

When any trip queued before the first signal, the diagram starts upstream of
it at the **back of the longest queue**, plus 50 m. A queue is measured from
where the trip first slowed below 8 km/h to the stop line, through stops and
crawling; a stop the phone matched to the same signal also counts, so a
queue that took two cycles is measured from its first stop. The description
under the title says how far back the diagram starts and which trip had the
longest queue.

A single trip shows the queue when it arrived — the queue may have grown
behind it — so the longest queue across many trips is the best estimate of
the maximum.

**Tick trips in the legend** to pick them out: ticked trips are drawn on top
and thicker on every chart and on the map, and the rest fade. **Show all**
clears the ticks.

### Speed along the route

GPS speed along the baseline's route, every trip overlaid, lined up by
distance.

### Section times

Each trip's time between consecutive checkpoints, against the baseline:
**blue is faster, red is slower**. Hover a time to see its stops. "—" means
the trip didn't drive that section. **Fastest**, **Mean** and **Spread**
(slowest minus fastest) show where trips differ most; the last row is the
whole span or stretch.

### Routes and checkpoints

Every trip's route on the map, with the numbered checkpoints; those inside the
compared stretch are highlighted. Click a checkpoint to start or end the
stretch there.

## Settings

- **Trip library**: how many trips and libraries there are, the last import,
  where the library is stored. **Import database…**, **Open data folder**
  (with its backups), and **Save a copy to Downloads**.
- **Units**: **Metric**, **Imperial**, or **Custom** (speed, distance and
  acceleration set separately).
- **Appearance**: **System**, **Light** or **Dark**.
- **Traffic signal datasets**: the regional signal datasets used to name
  signals and crossings when a trip is checked. They are refreshed
  automatically once a week from the government open-data portals (when the
  app opens), so newly commissioned signals are picked up without a new
  version; the screen shows when each was last updated.
- **Segment splitting**: whether long moving stretches are split **By road**
  (at each change of road) or **By signal/crossing** (at each signal and
  crossing passed, and at a turn onto another road that the map confirms).
  Applies to trips checked from then on.
- **Trip details**: how many trips still have road names, cross streets or
  signals to look up; **Resolve now** looks them all up online
  (OpenStreetMap's Overpass and Nominatim, OSRM, and Valhalla when Overpass
  is unavailable). It can take a few minutes per trip; **Stop** ends it
  early. If some trips can't be checked, it says how many and why — the
  rest are still saved — so run it again later for those.
- **Export trips**: a zip of every trip's CSV, XLSX and GPX — the last 7, 30,
  90, 180 or 365 days, or all trips — saved to `Downloads\Nomad`.
- **Delete trips**: remove trips older than 30, 90, 180 or 365 days from this
  PC.

## About and updates

**About** shows the version, data sources and the privacy policy.

The app checks for a new version when it starts (at most twice a day; switch
this off under **Check for updates automatically**). When one is available,
the update bar offers **Update now**: it downloads the installer, checks it
against the published checksum, installs it and reopens the app. Your trips
and libraries are kept. **About → Check for updates** checks straight away.

## Arranging the window

- **Drag a divider** between panes, or the grip under a chart or map, to
  resize it; **double-click** it to reset. Sizes are remembered.
- **Collapse a section** on the Compare page with the **⌃** at its top
  right.
- Wide tables scroll sideways; long names are shortened with "…" and shown in
  full on hover.

## Glossary

- **Baseline** — the trip every other trip is measured against; its route
  defines the checkpoints.
- **Checkpoint** — a timing point on the baseline's route: a signal,
  crossing, intersection or fixed distance, numbered from the start.
- **Common span** — from the first to the last checkpoint every compared trip
  passed.
- **Stretch** — part of the route you picked to compare on its own.
- **Section** — the route between two consecutive checkpoints.
- **Queue** — where a trip slowed below 8 km/h before a stop line until it
  went over the line.
- **Congestion episode** — two or more stops joined by crawling traffic.
- **Control delay** — the time a congestion episode cost compared with
  free-flowing traffic (HCM method), graded as a **level of service**.

## Troubleshooting

- **"Windows protected your PC" when installing** — choose **More info → Run
  anyway**.
- **The phone doesn't see this computer over Wi-Fi** — keep the **Receive**
  page open, check both are on the same network, allow the app on private
  networks, or enter an address shown on the Receive page into the phone.
- **The phone on a USB cable isn't picked up** — unlock it and choose **File
  transfer** (not *Charging only*) in its USB notification.
- **Trips show details still to resolve** — the online map services may be
  busy; use **Settings → Trip details → Resolve now** later.
- **A trip is missing from a comparison's charts** — it didn't drive the
  compared span; the notes above the summary say which trips and why.
