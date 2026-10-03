Kotya Job Schedule — installable web app (PWA) for Maria's shifts

Shift codes from the "grafik" Excel (the "Maria" column):
- rano      = morning, 07:00–15:00
- wieczór   = evening, 14:00–22:00
- do 13:00  = until 13:00 (starts at 07:00)
- od 17     = from 17:00 (until 22:00)
- 7-9/12-16:30 = split shift
- "-"       = day off
Change these in SHIFTS / parseEntry in index.html if they differ.

New month: press "Update source" and pick the new grafik .xlsx. It replaces the current schedule
(only one schedule is kept). Its day numbers are shown in the current calendar month.

A PWA must be served over HTTPS (or localhost). Pick one:

1) GitHub Pages: create a repo, upload all files from this folder (keep the icons/ folder),
   Settings -> Pages -> Deploy from branch (main, / root). Open https://<you>.github.io/<repo>/
2) Netlify Drop: drag this folder onto https://app.netlify.com/drop
3) Local test: in this folder run  python3 -m http.server 8000  and open http://localhost:8000

Install:
- Android / desktop Chrome or Edge: browser menu -> Install app (or Add to Home screen).
- iPhone / iPad (Safari): Share -> Add to Home Screen.

After editing index.html, change VERSION in sw.js so phones pick up the new version.
