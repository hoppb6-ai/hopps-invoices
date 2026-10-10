# Hopp (formerly Hopps Invoices)

Self-contained local invoice builder. No internet required after first load. No accounts. No servers.

## How to install on iPhone

1. Open the hosted URL in Safari.
2. Tap the Share button → Add to Home Screen.
3. Name it "Hopp".
4. Open the icon. Enter PIN: 5295

Edit the profile first to put your real info in.

## Version 2 features
- Profile changes need your PIN plus typing SAVE.
- Log & Calendar: day job / side project / journal dots, month summary; invoices auto-log.
- Invoices get numbers (HOP-0001...). Customer Copy PNG and My File Copy PNG (private notes only on file copy).
- Invoice history with search, reopen, duplicate, paid/unpaid.
- Customers address book, editable catalogue, earnings dashboard.
- Backup: download a JSON file and restore it on a new phone.
- Auto-locks after 5 minutes in the background. All data stays on the phone (localStorage).

## Version 3 features
- Quotes / estimates (Q-0001...) with status and "Valid until"; Estimate PNG; convert to invoice or create a job in one tap.
- Jobs: status (Lead to Paid), scheduled date, start/stop timer, manual hours, materials, linked quotes and invoices; create an invoice from a job.
- Calendar shows scheduled jobs and days you logged job time.
- Example data: load from the first-run card or Backup & Examples; marked EXAMPLE and removable without touching real data.

## Version 4 features
- The app opens on the Calendar after the PIN. Bottom tabs: Calendar, Business (invoices, quotes, jobs, customers, earnings), Notes, More (settings, profile, backup).
- Calendar modes: Work, Side Biz, Personal, and All (every mode's dots together). Month or week view, a Today button, swipe to change month/week, long-press a day (or tap +) for quick add.
- Work (Boiler Operator at Northwest Hardwoods; change these in More): worked yes/no, shift (Day/Swing/Night/Custom), start/end, break, hours worked out automatically, overtime over 8 h/day and over 40 h/week, day type (Regular/OT/PTO/Sick/Holiday/Off), optional boiler log, notes. Month and pay-period totals; add an hourly wage in More to see estimated gross. Clock in / Clock out button for today.
- Side Biz: the same side-project, invoice, job and quote tracking as before.
- Personal: events/appointments/reminders (title, time, Family/Health/Errands/Other, notes), mood and energy, journal.
- Notes tab: search every mode's notes, filter by mode or tag, pinned notes first; tap a note to open its day.
- Version 3 data is upgraded automatically: old "Went to work" days move into the Work calendar.

## Version 4.1
- New NWH tab (Northwest Hardwoods): opens the Work calendar on today with Clock in/out and the pay-period summary at the top. Change the tab's short name in More, next to the employer.
- Quick add is now the "+ Add" button next to Today. The header shows a short "Hopp" title.

## Version 4.2
- AOCs (Abnormal Operating Conditions): log date/time, equipment (Boiler 1, Boiler 2, Both, Other), title, Probable vs Actual, severity, actions, status and resolved date, plus tags. Open the full searchable list from the NWH tab. AOCs show as a diamond marker on the calendar (red = high and still open).
- Daily checklist on the NWH tab and in each work day: meter reading, boiler systems checks, chemical tests per boiler (sulfite, pH, conductivity), overall check, blowdown time. Ticking an item records the time. Edit items, units and normal ranges in More; "Readings history" compares recent values and shows out-of-range ones in red.
- Chemical-test and blowdown notes from the old boiler log were moved into the checklist automatically.

v4.3 — Data safety
- Automatic snapshots (IndexedDB, localStorage fallback): taken when the app is hidden/closed, every 3 minutes while open, and a few seconds after saves. Keeps the last 10 plus one per day for 7 days. Broken or empty data is never snapshotted.
- 💾 Save (header and More): full backup JSON. Uses the file picker to save over the same file where supported, the iOS share sheet (Save to Files) where available, otherwise a download. Default name Hopps-Backup-YYYY-MM-DD.json; Save As remembers a custom name.
- More → Restore: restore any snapshot or a backup file. Current data is snapshotted first.
- On startup, if saved data is damaged or missing and snapshots exist, the app offers to restore the latest one.
- Reminder banner if no backup file has been saved in 3+ days (dismissible).

v4.4
- App renamed "Hopp" (title, home-screen name, PIN screen, header). Invoices still show the business name from the profile.
- New ordered NWH daily checklist (numbered): Fill Evap Tank, Collect water samples, 7 meters (gas, Boiler 2 gas, day bin cycle, Boiler 2/Boiler 1/Scrubber hour meters, water), Boiler 1 and 2 system checks, Water sample check (optional sulfite/pH/conductivity for each boiler). Blowdown item removed.
- Meter fields take digits only (hour meters allow one decimal). Entering a value checks the item.
- Each meter shows the previous reading (with its date), today's reading and daily usage (with the number of days when there's a gap). Negative usage is shown in red.
- Meter history (NWH → Meters): readings, usage and 7/30-day average per day.
- Upgrade: the old default items are replaced. Values already recorded under them are kept, shown under "Earlier checklist items" on that day and in Readings history. Custom items are kept.
