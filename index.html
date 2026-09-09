<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Manual Talktime Productivity</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/PapaParse/5.4.1/papaparse.min.js"></script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Carlito:wght@400;700&display=swap');

:root {
  --bg: #F3F2F1;
  --surface: #FFFFFF;
  --line: #E1E1E1;
  --line-strong: #C8C6C4;
  --ink: #252423;
  --ink-soft: #605E5C;
  --ink-faint: #A19F9D;
  --teal: #E31B4C;
  --teal-dark: #B8123D;
  --teal-soft: rgba(227,27,76,0.08);
  --flag: #252423;
  --flag-soft: rgba(37,36,35,0.06);
  --font-ui: Calibri, Carlito, 'Segoe UI', Arial, sans-serif;
  --font-display: Calibri, Carlito, 'Segoe UI', Arial, sans-serif;
  --font-num: Calibri, Carlito, 'Segoe UI', Arial, sans-serif;
  --shadow-sm: 0 1.2px 3.6px rgba(0,0,0,0.13), 0 0.6px 1.8px rgba(0,0,0,0.10);
  --shadow-md: 0 3.2px 7.2px rgba(0,0,0,0.13), 0 0.6px 1.8px rgba(0,0,0,0.10);
  --radius: 4px;
}

* { box-sizing: border-box; }
body { margin: 0; background: var(--bg); color: var(--ink); font-family: var(--font-ui); text-align: center; }

.wrap { max-width: 980px; margin: 0 auto; padding: 0 16px 60px; }

.top {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
  background: var(--surface);
  border-bottom: 1px solid var(--line);
  border-top: 4px solid var(--teal);
  padding: 18px 16px 16px;
  margin: 0 -16px 20px;
}
.badge {
  width: 34px; height: 34px;
  border: 2px solid var(--teal);
  border-radius: 50%;
  display: flex; align-items: center; justify-content: center;
  font-family: var(--font-display);
  font-weight: 700;
  font-size: 11px;
  color: var(--teal);
  margin-bottom: 2px;
}
.top h1 { font-family: var(--font-display); color: var(--ink); font-size: 20px; font-weight: 700; margin: 0; }
.top p { margin: 0; font-size: 12.5px; color: var(--ink-soft); }
.top .top-controls { margin-top: 8px; }

.upload-zone {
  border: 1px solid var(--line-strong);
  padding: 7px 14px;
  font-size: 12px;
  color: var(--ink-soft);
  cursor: pointer;
  border-radius: var(--radius);
  text-align: center;
  white-space: nowrap;
  background: var(--surface);
  transition: all 0.12s ease;
}
.upload-zone:hover { border-color: var(--teal); color: var(--teal); background: var(--teal-soft); }
.upload-zone.dragover { border-color: var(--teal); background: var(--teal-soft); color: var(--teal); }
#file-input { display: none; }

.top-controls { display: flex; gap: 8px; align-items: center; justify-content: center; flex-wrap: wrap; }
.tl-select {
  font-family: var(--font-ui);
  font-size: 12px;
  padding: 6px 10px;
  border: 1px solid var(--line-strong);
  border-radius: var(--radius);
  background: var(--surface);
  color: var(--ink);
}
.manage-btn {
  font-family: var(--font-ui);
  font-size: 12px;
  padding: 6px 12px;
  border: 1px solid var(--line-strong);
  border-radius: var(--radius);
  background: var(--surface);
  color: var(--ink-soft);
  cursor: pointer;
  white-space: nowrap;
  transition: all 0.12s ease;
}
.manage-btn:hover { border-color: var(--teal); color: var(--teal); background: var(--teal-soft); }

.modal-backdrop {
  position: fixed; inset: 0;
  background: rgba(37,36,35,0.4);
  display: flex; align-items: center; justify-content: center;
  padding: 20px; z-index: 20;
}
.modal {
  background: #FFFFFF;
  border: 1px solid var(--line-strong);
  border-top: 3px solid var(--teal);
  border-radius: var(--radius);
  box-shadow: var(--shadow-md);
  max-width: 480px; width: 100%;
  max-height: 82vh;
  overflow-y: auto;
  padding: 20px;
  text-align: center;
}
.modal h2 { font-size: 15px; font-weight: 700; margin: 0 0 4px; color: var(--ink); }
.modal .sub { font-size: 12px; color: var(--ink-soft); margin: 0 0 14px; }
.tl-add-row { display: flex; justify-content: center; gap: 8px; margin-bottom: 14px; }
.tl-add-row input {
  flex: 1;
  max-width: 260px;
  font-family: var(--font-ui);
  font-size: 12.5px;
  padding: 6px 9px;
  border: 1px solid var(--line-strong);
  border-radius: var(--radius);
  text-align: center;
  background: #FAFAFA;
}
.assign-row {
  display: grid; grid-template-columns: 1fr 1fr; justify-items: center; align-items: center;
  gap: 10px; padding: 7px 0; border-bottom: 1px solid var(--line);
}
.assign-row .name { font-size: 12.5px; text-align: center; color: var(--ink); }
.assign-row select {
  font-family: var(--font-ui);
  font-size: 12px;
  padding: 5px 7px;
  border: 1px solid var(--line-strong);
  border-radius: var(--radius);
  background: #FAFAFA;
  color: var(--ink);
  min-width: 150px;
  text-align: center;
  text-align-last: center;
}
.modal-actions { display: flex; justify-content: center; margin-top: 16px; }
.modal-actions button {
  font-family: var(--font-ui);
  font-size: 12.5px;
  padding: 6px 16px;
  border: 1px solid var(--teal);
  background: var(--teal);
  color: #fff;
  border-radius: var(--radius);
  cursor: pointer;
}
.modal-actions button:hover { background: var(--teal-dark); border-color: var(--teal-dark); }

.stats {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 12px;
  margin-bottom: 20px;
}
.stat {
  padding: 14px 12px;
  text-align: center;
  background: var(--surface);
  border: 1px solid var(--line);
  border-left: 3px solid var(--teal);
  border-radius: var(--radius);
  box-shadow: var(--shadow-sm);
}
.stat-icon { font-size: 15px; margin-bottom: 4px; }
.stat-label { font-size: 11px; font-weight: 700; text-transform: uppercase; letter-spacing: 0.3px; color: var(--ink-soft); margin-bottom: 4px; }
.stat-value { font-family: var(--font-num); font-size: 22px; font-weight: 700; color: var(--ink); }
@media (max-width: 640px) {
  .stats { grid-template-columns: repeat(2, 1fr); }
}

.section-head {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-bottom: 10px;
  gap: 8px;
  flex-wrap: wrap;
}
.section-head h2 { font-family: var(--font-display); font-size: 14px; font-weight: 700; margin: 0; color: var(--ink); }

.chart-block {
  margin-bottom: 22px;
  background: var(--surface);
  border: 1px solid var(--line);
  border-radius: var(--radius);
  box-shadow: var(--shadow-sm);
  padding: 16px;
}
.chart-block .section-head { margin-bottom: 14px; }
.bar-row { display: flex; align-items: center; justify-content: center; gap: 10px; padding: 5px 0; max-width: 560px; margin: 0 auto; }
.bar-rank { width: 20px; flex-shrink: 0; font-size: 12px; text-align: center; }
.bar-name { width: 140px; flex-shrink: 0; font-size: 12px; color: var(--ink-soft); text-align: center; overflow: hidden; text-overflow: ellipsis; white-space: nowrap; }
.bar-track { flex: 1; height: 12px; background: #EDEBE9; border-radius: 2px; position: relative; overflow: hidden; }
.bar-fill { height: 100%; border-radius: 2px; background: var(--teal); transition: width 0.4s ease; }
.bar-fill.low { background: var(--flag); }
.bar-value { width: 68px; flex-shrink: 0; font-family: var(--font-num); font-size: 12px; font-weight: 700; color: var(--ink); text-align: center; }

.tabs { display: flex; gap: 0; justify-content: center; border-bottom: 1px solid var(--line); }
.tab-btn {
  font-family: var(--font-ui);
  font-size: 12.5px;
  font-weight: 600;
  padding: 8px 18px;
  border: none;
  border-bottom: 3px solid transparent;
  background: transparent;
  color: var(--ink-soft);
  cursor: pointer;
  margin-bottom: -1px;
  transition: all 0.12s ease;
}
.tab-btn.active { color: var(--teal); border-bottom-color: var(--teal); }

.filters { display: flex; gap: 8px; align-items: center; justify-content: center; }
.filters select {
  font-family: var(--font-ui);
  font-size: 12px;
  padding: 6px 10px;
  border: 1px solid var(--line-strong);
  border-radius: var(--radius);
  background: var(--surface);
  color: var(--ink);
}

.table-card { background: var(--surface); border: 1px solid var(--line); border-radius: var(--radius); box-shadow: var(--shadow-sm); overflow: hidden; }
table { width: 100%; border-collapse: collapse; font-size: 12.5px; }
thead th {
  text-align: center;
  font-size: 11px;
  font-weight: 700;
  letter-spacing: 0.2px;
  color: var(--ink);
  background: #EDEBE9;
  padding: 9px 10px;
  border-bottom: 2px solid var(--line-strong);
  border-right: 1px solid var(--line);
  cursor: pointer;
  user-select: none;
  white-space: nowrap;
}
thead th:last-child { border-right: none; }
thead th:hover { color: var(--teal); background: #E4E2E0; }
thead th.sorted::after { content: ' \25BE'; }
thead th.sorted.asc::after { content: ' \25B4'; }
tbody td { padding: 8px 10px; border-bottom: 1px solid var(--line); border-right: 1px solid var(--line); text-align: center; }
tbody td:last-child { border-right: none; }
tbody tr:nth-child(even) { background: #FAF9F8; }
tbody td.num { font-family: var(--font-num); text-align: center; }
tbody tr:hover { background: #F3F2F1; }
tbody tr.below-avg td.num.avg-cell { color: var(--flag); }
tbody tr.above-avg td.num.avg-cell { color: var(--teal); font-weight: 700; }
tbody tr:last-child td { border-bottom: none; }
tbody tr.avg-row { background: var(--teal-soft); font-weight: 700; }
tbody tr.avg-row td { border-top: 2px solid var(--teal); border-bottom: none; color: var(--ink); }
tbody tr.avg-row:hover { background: var(--teal-soft); }

.empty { text-align: center; padding: 50px 20px; color: var(--ink-faint); font-size: 13px; border: 1px dashed var(--line-strong); border-radius: var(--radius); background: var(--surface); }
.foot-note { margin-top: 12px; font-size: 11px; color: var(--ink-faint); text-align: center; }
.site-credit {
  margin-top: 24px;
  padding-top: 14px;
  border-top: 1px solid var(--line);
  font-size: 11.5px;
  color: var(--ink-faint);
  text-align: center;
}
.site-credit a { color: var(--teal); text-decoration: none; font-weight: 700; }
.site-credit a:hover { text-decoration: underline; }
</style>
</head>
<body>
<div class="wrap" id="app">
  <div class="empty">Loading dataset…</div>
</div>

<script>
const STORAGE_KEY = 'manual-talktime-dataset';

const RAW_COLS = {
  callTime: 'Call Time',
  userId: 'User ID',
  userName: 'User Name',
  talk: 'User Talk Time',
  disposition: 'System Disposition'
};

let dataset = null; // { users: {id:name}, records: [...], teamLeaders: {tlId:name}, assignments: {userId:tlId} }
let view = 'byUser'; // 'byUser' | 'byDay'
let sortKey = 'avg';
let sortDir = 'desc';
let filterUser = 'all';
let filterDate = 'all';
let filterTL = 'all';
let showManageModal = false;

const DEFAULT_DATA = {"users": {"afrin.fulari@pw.live": "Afrin Abdul Fulari", "Priyanka.singh6@pw.live": "Priyanka Singh", "neetu.2@pw.live": "Neetu", "deepika.gupta@pw.live": "Deepika Gupta", "pooja.ambhore@pw.live": "Pooja Ambhore", "kritika.kumari@pw.live": "Kritika Kumari", "aman.rai1@pw.live": "Aman Rai1", "triloki.sharma@pw.live": "Triloki Sharma", "payal.ekunkar@pw.live": "Payal Ekunkar", "hemant.pramanik@pw.live": "Hemant Pramanik", "chandrahash.sonkar@pw.live": "Chandrahash Sonkar", "kuldeep.chandravanshi@pw.live": "Kuldeep Chandravanshi", "Gunjan.chandwani@pw.live": "Gunjan Chandwani", "shivansh.mehrotra@pw.live": "Shivansh Mehrotra"}, "records": [{"userId": "afrin.fulari@pw.live", "userName": "Afrin Abdul Fulari", "date": "2026-09-01", "dials": 35, "talkSeconds": 1776, "connected": 10}, {"userId": "aman.rai1@pw.live", "userName": "Aman Rai1", "date": "2026-09-01", "dials": 8, "talkSeconds": 500, "connected": 3}, {"userId": "chandrahash.sonkar@pw.live", "userName": "Chandrahash Sonkar", "date": "2026-09-01", "dials": 43, "talkSeconds": 2341, "connected": 12}, {"userId": "deepika.gupta@pw.live", "userName": "Deepika Gupta", "date": "2026-09-01", "dials": 38, "talkSeconds": 4150, "connected": 14}, {"userId": "hemant.pramanik@pw.live", "userName": "Hemant Pramanik", "date": "2026-09-01", "dials": 69, "talkSeconds": 2218, "connected": 23}, {"userId": "kritika.kumari@pw.live", "userName": "Kritika Kumari", "date": "2026-09-01", "dials": 60, "talkSeconds": 4168, "connected": 21}, {"userId": "kuldeep.chandravanshi@pw.live", "userName": "Kuldeep Chandravanshi", "date": "2026-09-01", "dials": 29, "talkSeconds": 1295, "connected": 11}, {"userId": "neetu.2@pw.live", "userName": "Neetu", "date": "2026-09-01", "dials": 22, "talkSeconds": 1380, "connected": 12}, {"userId": "payal.ekunkar@pw.live", "userName": "Payal Ekunkar", "date": "2026-09-01", "dials": 29, "talkSeconds": 2077, "connected": 13}, {"userId": "pooja.ambhore@pw.live", "userName": "Pooja Ambhore", "date": "2026-09-01", "dials": 13, "talkSeconds": 138, "connected": 2}, {"userId": "Priyanka.singh6@pw.live", "userName": "Priyanka Singh", "date": "2026-09-01", "dials": 25, "talkSeconds": 3214, "connected": 11}, {"userId": "triloki.sharma@pw.live", "userName": "Triloki Sharma", "date": "2026-09-01", "dials": 86, "talkSeconds": 4575, "connected": 25}, {"userId": "afrin.fulari@pw.live", "userName": "Afrin Abdul Fulari", "date": "2026-09-02", "dials": 42, "talkSeconds": 4102, "connected": 17}, {"userId": "aman.rai1@pw.live", "userName": "Aman Rai1", "date": "2026-09-02", "dials": 9, "talkSeconds": 958, "connected": 6}, {"userId": "chandrahash.sonkar@pw.live", "userName": "Chandrahash Sonkar", "date": "2026-09-02", "dials": 35, "talkSeconds": 3103, "connected": 12}, {"userId": "deepika.gupta@pw.live", "userName": "Deepika Gupta", "date": "2026-09-02", "dials": 32, "talkSeconds": 1899, "connected": 11}, {"userId": "Gunjan.chandwani@pw.live", "userName": "Gunjan Chandwani", "date": "2026-09-02", "dials": 71, "talkSeconds": 3645, "connected": 31}, {"userId": "hemant.pramanik@pw.live", "userName": "Hemant Pramanik", "date": "2026-09-02", "dials": 99, "talkSeconds": 3275, "connected": 37}, {"userId": "kuldeep.chandravanshi@pw.live", "userName": "Kuldeep Chandravanshi", "date": "2026-09-02", "dials": 55, "talkSeconds": 3997, "connected": 27}, {"userId": "neetu.2@pw.live", "userName": "Neetu", "date": "2026-09-02", "dials": 34, "talkSeconds": 1505, "connected": 16}, {"userId": "payal.ekunkar@pw.live", "userName": "Payal Ekunkar", "date": "2026-09-02", "dials": 28, "talkSeconds": 566, "connected": 5}, {"userId": "pooja.ambhore@pw.live", "userName": "Pooja Ambhore", "date": "2026-09-02", "dials": 17, "talkSeconds": 1480, "connected": 5}, {"userId": "Priyanka.singh6@pw.live", "userName": "Priyanka Singh", "date": "2026-09-02", "dials": 23, "talkSeconds": 2208, "connected": 13}, {"userId": "shivansh.mehrotra@pw.live", "userName": "Shivansh Mehrotra", "date": "2026-09-02", "dials": 49, "talkSeconds": 3308, "connected": 12}, {"userId": "triloki.sharma@pw.live", "userName": "Triloki Sharma", "date": "2026-09-02", "dials": 106, "talkSeconds": 4175, "connected": 26}, {"userId": "afrin.fulari@pw.live", "userName": "Afrin Abdul Fulari", "date": "2026-09-03", "dials": 35, "talkSeconds": 4065, "connected": 14}, {"userId": "aman.rai1@pw.live", "userName": "Aman Rai1", "date": "2026-09-03", "dials": 42, "talkSeconds": 2127, "connected": 14}, {"userId": "chandrahash.sonkar@pw.live", "userName": "Chandrahash Sonkar", "date": "2026-09-03", "dials": 62, "talkSeconds": 4462, "connected": 21}, {"userId": "deepika.gupta@pw.live", "userName": "Deepika Gupta", "date": "2026-09-03", "dials": 44, "talkSeconds": 4050, "connected": 24}, {"userId": "Gunjan.chandwani@pw.live", "userName": "Gunjan Chandwani", "date": "2026-09-03", "dials": 39, "talkSeconds": 10530, "connected": 18}, {"userId": "hemant.pramanik@pw.live", "userName": "Hemant Pramanik", "date": "2026-09-03", "dials": 122, "talkSeconds": 3884, "connected": 35}, {"userId": "kritika.kumari@pw.live", "userName": "Kritika Kumari", "date": "2026-09-03", "dials": 66, "talkSeconds": 4113, "connected": 13}, {"userId": "kuldeep.chandravanshi@pw.live", "userName": "Kuldeep Chandravanshi", "date": "2026-09-03", "dials": 86, "talkSeconds": 3976, "connected": 30}, {"userId": "neetu.2@pw.live", "userName": "Neetu", "date": "2026-09-03", "dials": 67, "talkSeconds": 3990, "connected": 24}, {"userId": "payal.ekunkar@pw.live", "userName": "Payal Ekunkar", "date": "2026-09-03", "dials": 60, "talkSeconds": 2552, "connected": 23}, {"userId": "pooja.ambhore@pw.live", "userName": "Pooja Ambhore", "date": "2026-09-03", "dials": 22, "talkSeconds": 3192, "connected": 7}, {"userId": "Priyanka.singh6@pw.live", "userName": "Priyanka Singh", "date": "2026-09-03", "dials": 33, "talkSeconds": 3665, "connected": 15}, {"userId": "shivansh.mehrotra@pw.live", "userName": "Shivansh Mehrotra", "date": "2026-09-03", "dials": 39, "talkSeconds": 3912, "connected": 14}, {"userId": "triloki.sharma@pw.live", "userName": "Triloki Sharma", "date": "2026-09-03", "dials": 76, "talkSeconds": 3998, "connected": 23}, {"userId": "afrin.fulari@pw.live", "userName": "Afrin Abdul Fulari", "date": "2026-09-04", "dials": 51, "talkSeconds": 3835, "connected": 17}, {"userId": "aman.rai1@pw.live", "userName": "Aman Rai1", "date": "2026-09-04", "dials": 53, "talkSeconds": 2334, "connected": 16}, {"userId": "chandrahash.sonkar@pw.live", "userName": "Chandrahash Sonkar", "date": "2026-09-04", "dials": 61, "talkSeconds": 4740, "connected": 15}, {"userId": "Gunjan.chandwani@pw.live", "userName": "Gunjan Chandwani", "date": "2026-09-04", "dials": 57, "talkSeconds": 3818, "connected": 22}, {"userId": "hemant.pramanik@pw.live", "userName": "Hemant Pramanik", "date": "2026-09-04", "dials": 84, "talkSeconds": 5147, "connected": 30}, {"userId": "kritika.kumari@pw.live", "userName": "Kritika Kumari", "date": "2026-09-04", "dials": 123, "talkSeconds": 4273, "connected": 34}, {"userId": "neetu.2@pw.live", "userName": "Neetu", "date": "2026-09-04", "dials": 64, "talkSeconds": 3725, "connected": 29}, {"userId": "pooja.ambhore@pw.live", "userName": "Pooja Ambhore", "date": "2026-09-04", "dials": 42, "talkSeconds": 3758, "connected": 13}, {"userId": "Priyanka.singh6@pw.live", "userName": "Priyanka Singh", "date": "2026-09-04", "dials": 68, "talkSeconds": 3834, "connected": 23}, {"userId": "shivansh.mehrotra@pw.live", "userName": "Shivansh Mehrotra", "date": "2026-09-04", "dials": 65, "talkSeconds": 5683, "connected": 20}, {"userId": "triloki.sharma@pw.live", "userName": "Triloki Sharma", "date": "2026-09-04", "dials": 98, "talkSeconds": 5259, "connected": 44}, {"userId": "chandrahash.sonkar@pw.live", "userName": "Chandrahash Sonkar", "date": "2026-09-05", "dials": 51, "talkSeconds": 2302, "connected": 8}, {"userId": "deepika.gupta@pw.live", "userName": "Deepika Gupta", "date": "2026-09-05", "dials": 43, "talkSeconds": 3791, "connected": 18}, {"userId": "Gunjan.chandwani@pw.live", "userName": "Gunjan Chandwani", "date": "2026-09-05", "dials": 58, "talkSeconds": 4517, "connected": 29}, {"userId": "hemant.pramanik@pw.live", "userName": "Hemant Pramanik", "date": "2026-09-05", "dials": 67, "talkSeconds": 5274, "connected": 32}, {"userId": "kritika.kumari@pw.live", "userName": "Kritika Kumari", "date": "2026-09-05", "dials": 42, "talkSeconds": 877, "connected": 9}, {"userId": "kuldeep.chandravanshi@pw.live", "userName": "Kuldeep Chandravanshi", "date": "2026-09-05", "dials": 86, "talkSeconds": 4194, "connected": 34}, {"userId": "neetu.2@pw.live", "userName": "Neetu", "date": "2026-09-05", "dials": 42, "talkSeconds": 3808, "connected": 18}, {"userId": "payal.ekunkar@pw.live", "userName": "Payal Ekunkar", "date": "2026-09-05", "dials": 35, "talkSeconds": 4082, "connected": 20}, {"userId": "pooja.ambhore@pw.live", "userName": "Pooja Ambhore", "date": "2026-09-05", "dials": 30, "talkSeconds": 2390, "connected": 13}, {"userId": "Priyanka.singh6@pw.live", "userName": "Priyanka Singh", "date": "2026-09-05", "dials": 26, "talkSeconds": 3721, "connected": 11}, {"userId": "shivansh.mehrotra@pw.live", "userName": "Shivansh Mehrotra", "date": "2026-09-05", "dials": 43, "talkSeconds": 3845, "connected": 16}, {"userId": "aman.rai1@pw.live", "userName": "Aman Rai1", "date": "2026-09-06", "dials": 55, "talkSeconds": 1225, "connected": 15}, {"userId": "chandrahash.sonkar@pw.live", "userName": "Chandrahash Sonkar", "date": "2026-09-06", "dials": 78, "talkSeconds": 3681, "connected": 20}, {"userId": "Gunjan.chandwani@pw.live", "userName": "Gunjan Chandwani", "date": "2026-09-06", "dials": 40, "talkSeconds": 1225, "connected": 14}, {"userId": "hemant.pramanik@pw.live", "userName": "Hemant Pramanik", "date": "2026-09-06", "dials": 74, "talkSeconds": 4023, "connected": 28}, {"userId": "kuldeep.chandravanshi@pw.live", "userName": "Kuldeep Chandravanshi", "date": "2026-09-06", "dials": 76, "talkSeconds": 4175, "connected": 34}, {"userId": "neetu.2@pw.live", "userName": "Neetu", "date": "2026-09-06", "dials": 26, "talkSeconds": 3863, "connected": 17}, {"userId": "pooja.ambhore@pw.live", "userName": "Pooja Ambhore", "date": "2026-09-06", "dials": 39, "talkSeconds": 3743, "connected": 19}, {"userId": "Priyanka.singh6@pw.live", "userName": "Priyanka Singh", "date": "2026-09-06", "dials": 54, "talkSeconds": 5776, "connected": 19}, {"userId": "shivansh.mehrotra@pw.live", "userName": "Shivansh Mehrotra", "date": "2026-09-06", "dials": 52, "talkSeconds": 3883, "connected": 10}, {"userId": "triloki.sharma@pw.live", "userName": "Triloki Sharma", "date": "2026-09-06", "dials": 121, "talkSeconds": 7895, "connected": 46}, {"userId": "aman.rai1@pw.live", "userName": "Aman Rai1", "date": "2026-09-07", "dials": 49, "talkSeconds": 2040, "connected": 11}, {"userId": "deepika.gupta@pw.live", "userName": "Deepika Gupta", "date": "2026-09-07", "dials": 23, "talkSeconds": 3878, "connected": 12}, {"userId": "Gunjan.chandwani@pw.live", "userName": "Gunjan Chandwani", "date": "2026-09-07", "dials": 53, "talkSeconds": 3559, "connected": 17}, {"userId": "hemant.pramanik@pw.live", "userName": "Hemant Pramanik", "date": "2026-09-07", "dials": 81, "talkSeconds": 3892, "connected": 33}, {"userId": "kritika.kumari@pw.live", "userName": "Kritika Kumari", "date": "2026-09-07", "dials": 66, "talkSeconds": 4267, "connected": 26}, {"userId": "kuldeep.chandravanshi@pw.live", "userName": "Kuldeep Chandravanshi", "date": "2026-09-07", "dials": 89, "talkSeconds": 4025, "connected": 27}, {"userId": "payal.ekunkar@pw.live", "userName": "Payal Ekunkar", "date": "2026-09-07", "dials": 20, "talkSeconds": 2764, "connected": 9}, {"userId": "pooja.ambhore@pw.live", "userName": "Pooja Ambhore", "date": "2026-09-07", "dials": 24, "talkSeconds": 4509, "connected": 9}, {"userId": "Priyanka.singh6@pw.live", "userName": "Priyanka Singh", "date": "2026-09-07", "dials": 44, "talkSeconds": 4336, "connected": 15}, {"userId": "shivansh.mehrotra@pw.live", "userName": "Shivansh Mehrotra", "date": "2026-09-07", "dials": 51, "talkSeconds": 4374, "connected": 15}, {"userId": "triloki.sharma@pw.live", "userName": "Triloki Sharma", "date": "2026-09-07", "dials": 76, "talkSeconds": 5526, "connected": 32}, {"userId": "afrin.fulari@pw.live", "userName": "Afrin Abdul Fulari", "date": "2026-09-08", "dials": 33, "talkSeconds": 4166, "connected": 10}, {"userId": "aman.rai1@pw.live", "userName": "Aman Rai1", "date": "2026-09-08", "dials": 12, "talkSeconds": 1437, "connected": 7}, {"userId": "chandrahash.sonkar@pw.live", "userName": "Chandrahash Sonkar", "date": "2026-09-08", "dials": 47, "talkSeconds": 3783, "connected": 18}, {"userId": "deepika.gupta@pw.live", "userName": "Deepika Gupta", "date": "2026-09-08", "dials": 11, "talkSeconds": 189, "connected": 1}, {"userId": "hemant.pramanik@pw.live", "userName": "Hemant Pramanik", "date": "2026-09-08", "dials": 59, "talkSeconds": 2609, "connected": 21}, {"userId": "kritika.kumari@pw.live", "userName": "Kritika Kumari", "date": "2026-09-08", "dials": 30, "talkSeconds": 1799, "connected": 11}, {"userId": "kuldeep.chandravanshi@pw.live", "userName": "Kuldeep Chandravanshi", "date": "2026-09-08", "dials": 51, "talkSeconds": 3153, "connected": 21}, {"userId": "neetu.2@pw.live", "userName": "Neetu", "date": "2026-09-08", "dials": 11, "talkSeconds": 558, "connected": 4}, {"userId": "payal.ekunkar@pw.live", "userName": "Payal Ekunkar", "date": "2026-09-08", "dials": 10, "talkSeconds": 1159, "connected": 2}, {"userId": "Priyanka.singh6@pw.live", "userName": "Priyanka Singh", "date": "2026-09-08", "dials": 33, "talkSeconds": 5519, "connected": 15}, {"userId": "triloki.sharma@pw.live", "userName": "Triloki Sharma", "date": "2026-09-08", "dials": 83, "talkSeconds": 4890, "connected": 23}]}
;

function toSeconds(hms) {
  if (!hms) return 0;
  const p = hms.split(':');
  if (p.length !== 3) return 0;
  return (+p[0]) * 3600 + (+p[1]) * 60 + (+p[2]);
}

function humanizeName(id) {
  const prefix = id.split('@')[0];
  return prefix.replace(/[._]/g, ' ').split(' ')
    .filter(Boolean)
    .map(w => w.replace(/\d+$/, ''))
    .filter(Boolean)
    .map(w => w.charAt(0).toUpperCase() + w.slice(1))
    .join(' ') || prefix;
}

function aggregateRaw(rows) {
  const agg = {};
  const users = {};
  for (const row of rows) {
    const uid = (row[RAW_COLS.userId] || '').trim();
    if (!uid) continue;
    let uname = (row[RAW_COLS.userName] || '').trim();
    if (!uname || uname.toLowerCase() === uid.toLowerCase()) {
      uname = humanizeName(uid);
    }
    users[uid] = uname;
    const callTime = row[RAW_COLS.callTime] || '';
    const datePart = callTime.split(' ')[0];
    const dm = datePart.split('-');
    if (dm.length !== 3) continue;
    const iso = `${dm[2]}-${dm[1]}-${dm[0]}`;
    const key = uid + '|' + iso;
    if (!agg[key]) agg[key] = { userId: uid, date: iso, dials: 0, talkSeconds: 0, connected: 0 };
    agg[key].dials += 1;
    agg[key].talkSeconds += toSeconds(row[RAW_COLS.talk]);
    if (row[RAW_COLS.disposition] === 'CONNECTED') agg[key].connected += 1;
  }
  const records = Object.values(agg).map(r => ({ ...r, userName: users[r.userId] }));
  records.sort((a, b) => a.date.localeCompare(b.date) || a.userName.localeCompare(b.userName));
  return { users, records, teamLeaders: {}, assignments: {} };
}

function ensureTLFields(ds) {
  if (!ds.teamLeaders) ds.teamLeaders = {};
  if (!ds.assignments) ds.assignments = {};
  return ds;
}

function fmtDuration(totalSeconds) {
  const s = Math.round(totalSeconds);
  const h = Math.floor(s / 3600);
  const m = Math.floor((s % 3600) / 60);
  const sec = s % 60;
  if (h > 0) return `${h}h ${String(m).padStart(2,'0')}m`;
  return `${m}m ${String(sec).padStart(2,'0')}s`;
}

function fmtDate(iso) {
  const [y,m,d] = iso.split('-');
  return `${d}-${m}-${y}`;
}

async function loadStored() {
  try {
    const res = await window.storage.get(STORAGE_KEY, true);
    if (res && res.value) {
      dataset = ensureTLFields(JSON.parse(res.value));
      return;
    }
  } catch (e) { /* nothing stored yet */ }
  dataset = ensureTLFields(DEFAULT_DATA);
}

async function saveStored() {
  try { await window.storage.set(STORAGE_KEY, JSON.stringify(dataset), true); }
  catch (e) { console.error('Storage error:', e); }
}

function byUserRows() {
  const byUser = {};
  for (const r of tlFilteredRecords()) {
    if (!byUser[r.userId]) byUser[r.userId] = { userId: r.userId, userName: r.userName, dials: 0, talkSeconds: 0, connected: 0, days: new Set() };
    byUser[r.userId].dials += r.dials;
    byUser[r.userId].talkSeconds += r.talkSeconds;
    byUser[r.userId].connected += r.connected;
    byUser[r.userId].days.add(r.date);
  }
  return Object.values(byUser).map(u => ({
    ...u,
    days: u.days.size,
    avg: u.dials ? u.talkSeconds / u.dials : 0
  }));
}

function byDayRows() {
  return tlFilteredRecords()
    .filter(r => filterUser === 'all' || r.userId === filterUser)
    .filter(r => filterDate === 'all' || r.date === filterDate)
    .map(r => ({ ...r, avg: r.dials ? r.talkSeconds / r.dials : 0 }));
}

function render() {
  const app = document.getElementById('app');
  if (!dataset || dataset.records.length === 0) {
    app.innerHTML = `
      <div class="top">
        <div class="badge">PW</div>
        <div><h1>Manual Talktime Productivity</h1><p>Average talktime per dial, by user and day.</p></div>
        <div class="upload-zone" id="upload-zone">Drop a call-detail CSV, or click to browse<input type="file" id="file-input" accept=".csv"></div>
      </div>
      <div class="empty">No data loaded yet. Upload a call-detail export to get started.</div>
      <p class="site-credit">Created by Wasil — for any help or suggestions, please connect <a href="mailto:wasil.khan@pw.live">wasil.khan@pw.live</a></p>
    `;
    wireUpload();
    return;
  }

  const scoped = tlFilteredRecords();
  const totalDials = scoped.reduce((a,r) => a + r.dials, 0);
  const totalTalk = scoped.reduce((a,r) => a + r.talkSeconds, 0);
  const dates = [...new Set(scoped.map(r => r.date))].sort();
  const avgAll = totalDials ? totalTalk / totalDials : 0;
  const userCount = new Set(scoped.map(r => r.userId)).size;
  const tlEntries = Object.entries(dataset.teamLeaders);

  const userRows = byUserRows().sort((a,b) => b.avg - a.avg);
  const maxAvg = Math.max(...userRows.map(u => u.avg), 1);

  app.innerHTML = `
    <div class="top">
      <div class="badge">PW</div>
      <div><h1>Manual Talktime Productivity</h1><p>Average talktime per dial, by user and day.</p></div>
      <div class="top-controls">
        <select class="tl-select" id="filter-tl">
          <option value="all">All team leaders</option>
          ${tlEntries.map(([id,name]) => `<option value="${id}" ${filterTL===id?'selected':''}>${esc(name)}</option>`).join('')}
        </select>
        <button class="manage-btn" id="manage-tl-btn">Manage TLs</button>
        <div class="upload-zone" id="tl-map-zone">Import TL mapping CSV<input type="file" id="tl-map-input" accept=".csv"></div>
        <div class="upload-zone" id="upload-zone">Drop a new CSV, or click to browse<input type="file" id="file-input" accept=".csv"></div>
      </div>
    </div>
    ${renderManageModal()}

    <div class="stats">
      <div class="stat"><div class="stat-icon">📞</div><div class="stat-label">Total dials</div><div class="stat-value">${totalDials.toLocaleString()}</div></div>
      <div class="stat"><div class="stat-icon">⏱️</div><div class="stat-label">Total talktime</div><div class="stat-value">${fmtDuration(totalTalk)}</div></div>
      <div class="stat"><div class="stat-icon">📊</div><div class="stat-label">Team avg / dial</div><div class="stat-value">${fmtDuration(avgAll)}</div></div>
      <div class="stat"><div class="stat-icon">👥</div><div class="stat-label">Users · days</div><div class="stat-value">${userCount} · ${dates.length}</div></div>
    </div>

    <div class="chart-block">
      <div class="section-head"><h2>Avg talktime per dial, by user</h2></div>
      ${userRows.map((u,i) => `
        <div class="bar-row">
          <div class="bar-rank">${i===0?'🥇':i===1?'🥈':i===2?'🥉':''}</div>
          <div class="bar-name">${esc(u.userName)}</div>
          <div class="bar-track"><div class="bar-fill ${u.avg < avgAll ? 'low' : ''}" style="width:${(u.avg/maxAvg*100).toFixed(1)}%"></div></div>
          <div class="bar-value">${fmtDuration(u.avg)}</div>
        </div>
      `).join('')}
    </div>

    <div class="section-head">
      <div class="tabs">
        <button class="tab-btn ${view==='byUser'?'active':''}" data-view="byUser">By user</button>
        <button class="tab-btn ${view==='byDay'?'active':''}" data-view="byDay">By day</button>
      </div>
      ${view === 'byDay' ? `
        <div class="filters">
          <select id="filter-user">
            <option value="all">All users</option>
            ${Object.entries(dataset.users)
              .filter(([id]) => filterTL === 'all' || dataset.assignments[id] === filterTL)
              .map(([id,name]) => `<option value="${id}" ${filterUser===id?'selected':''}>${esc(name)}</option>`).join('')}
          </select>
          <select id="filter-date">
            <option value="all">All dates</option>
            ${dates.map(d => `<option value="${d}" ${filterDate===d?'selected':''}>${fmtDate(d)}</option>`).join('')}
          </select>
        </div>
      ` : ''}
    </div>

    <div class="table-card">${renderTable(avgAll)}</div>

    <p class="foot-note">Avg / dial = total talktime ÷ total dials for that row. Crimson marks above the team average, black marks below it.</p>

    <p class="site-credit">Created by Wasil — for any help or suggestions, please connect <a href="mailto:wasil.khan@pw.live">wasil.khan@pw.live</a></p>
  `;

  wireUpload();
  wireManageModal();
  const ftl = document.getElementById('filter-tl');
  if (ftl) ftl.addEventListener('change', () => { filterTL = ftl.value; filterUser = 'all'; render(); });
  const manageBtn = document.getElementById('manage-tl-btn');
  if (manageBtn) manageBtn.addEventListener('click', openManageModal);
  document.querySelectorAll('.tab-btn').forEach(b => b.addEventListener('click', () => { view = b.dataset.view; render(); }));
  const fu = document.getElementById('filter-user');
  if (fu) fu.addEventListener('change', () => { filterUser = fu.value; render(); });
  const fd = document.getElementById('filter-date');
  if (fd) fd.addEventListener('change', () => { filterDate = fd.value; render(); });
  document.querySelectorAll('th[data-sort]').forEach(th => {
    th.addEventListener('click', () => {
      const key = th.dataset.sort;
      if (sortKey === key) sortDir = sortDir === 'asc' ? 'desc' : 'asc';
      else { sortKey = key; sortDir = 'desc'; }
      render();
    });
  });
}

function renderTable(avgAll) {
  let rows = view === 'byUser' ? byUserRows() : byDayRows();
  rows.sort((a,b) => {
    const va = a[sortKey], vb = b[sortKey];
    const cmp = typeof va === 'string' ? va.localeCompare(vb) : va - vb;
    return sortDir === 'asc' ? cmp : -cmp;
  });

  const cols = view === 'byUser'
    ? [['userName','User'],['dials','Dials'],['talkSeconds','Talktime'],['avg','Avg / dial'],['connected','Connected'],['days','Days']]
    : [['date','Date'],['userName','User'],['dials','Dials'],['talkSeconds','Talktime'],['avg','Avg / dial'],['connected','Connected']];

  if (rows.length === 0) return `<div class="empty">No rows match the current filters.</div>`;

  const avgDials = rows.reduce((a,r) => a + r.dials, 0) / rows.length;
  const avgTalk = rows.reduce((a,r) => a + r.talkSeconds, 0) / rows.length;
  const avgConnected = rows.reduce((a,r) => a + r.connected, 0) / rows.length;

  return `
    <table>
      <thead><tr>
        ${cols.map(([key,label]) => `<th data-sort="${key}" class="${sortKey===key?'sorted '+sortDir:''}">${label}</th>`).join('')}
      </tr></thead>
      <tbody>
        ${rows.map(r => `
          <tr class="${r.avg < avgAll ? 'below-avg' : 'above-avg'}">
            ${cols.map(([key]) => {
              if (key === 'userName') return `<td>${esc(r.userName)}</td>`;
              if (key === 'date') return `<td>${fmtDate(r.date)}</td>`;
              if (key === 'talkSeconds') return `<td class="num">${fmtDuration(r[key])}</td>`;
              if (key === 'avg') return `<td class="num avg-cell">${fmtDuration(r[key])}</td>`;
              return `<td class="num">${r[key]}</td>`;
            }).join('')}
          </tr>
        `).join('')}
        <tr class="avg-row">
          ${cols.map(([key]) => {
            if (key === 'userName' || key === 'date') return `<td>Average</td>`;
            if (key === 'dials') return `<td class="num">${Math.round(avgDials)}</td>`;
            if (key === 'talkSeconds') return `<td class="num">${fmtDuration(avgTalk)}</td>`;
            if (key === 'avg') return `<td class="num">${fmtDuration(avgAll)}</td>`;
            if (key === 'connected') return `<td class="num">${Math.round(avgConnected)}</td>`;
            return `<td class="num">—</td>`;
          }).join('')}
        </tr>
      </tbody>
    </table>
  `;
}

function esc(s) {
  const d = document.createElement('div');
  d.textContent = s == null ? '' : s;
  return d.innerHTML;
}

function wireUpload() {
  const zone = document.getElementById('upload-zone');
  const input = document.getElementById('file-input');
  wireDropZone(zone, input, handleFile);

  const tlZone = document.getElementById('tl-map-zone');
  const tlInput = document.getElementById('tl-map-input');
  wireDropZone(tlZone, tlInput, handleTLMappingFile);
}

function wireDropZone(zone, input, handler) {
  if (!zone || !input) return;
  zone.addEventListener('click', () => input.click());
  input.addEventListener('change', () => { if (input.files[0]) handler(input.files[0]); });
  ['dragover','dragenter'].forEach(ev => zone.addEventListener(ev, e => { e.preventDefault(); zone.classList.add('dragover'); }));
  ['dragleave','drop'].forEach(ev => zone.addEventListener(ev, e => { e.preventDefault(); zone.classList.remove('dragover'); }));
  zone.addEventListener('drop', e => { if (e.dataTransfer.files[0]) handler(e.dataTransfer.files[0]); });
}

const NAME_COL_CANDIDATES = ['counselor', 'counsellor', 'agent', 'user name', 'username', 'name', 'employee name', 'rep', 'member name', 'member'];
const TL_COL_CANDIDATES = ['tl name', 'tl', 'team leader', 'teamleader', 'team lead', 'manager', 'tl email', 'tl id', 'tl_email'];

function findColumn(headerRow, candidates) {
  const keys = Object.keys(headerRow);
  for (const cand of candidates) {
    const hit = keys.find(k => k.trim().toLowerCase() === cand);
    if (hit) return hit;
  }
  return null;
}

function normalize(s) {
  return (s || '').toString().trim().toLowerCase().replace(/\s+/g, ' ');
}

function displayNameFor(raw) {
  return raw.includes('@') ? humanizeName(raw) : raw;
}

function handleTLMappingFile(file) {
  Papa.parse(file, {
    header: true,
    skipEmptyLines: true,
    complete: (results) => {
      const rows = results.data;
      if (rows.length === 0) { alert('That file looks empty.'); return; }

      const nameCol = findColumn(rows[0], NAME_COL_CANDIDATES);
      const tlCol = findColumn(rows[0], TL_COL_CANDIDATES);
      if (!nameCol || !tlCol) {
        alert('Could not find a member-name column and a TL column in that file. Expected headers like "Member Name" and "TL Email" (or "Counselor" / "TL Name").');
        return;
      }

      // index existing users by normalized name and by id for matching
      const byNormName = {};
      const byNormId = {};
      for (const [uid, uname] of Object.entries(dataset.users)) {
        byNormName[normalize(uname)] = uid;
        byNormId[normalize(uid)] = uid;
      }

      let matched = 0, unmatched = [];
      for (const row of rows) {
        const rawName = (row[nameCol] || '').trim();
        const rawTL = (row[tlCol] || '').trim();
        if (!rawName || !rawTL) continue;

        const uid = byNormName[normalize(rawName)] || byNormId[normalize(rawName)];
        if (!uid) { unmatched.push(rawName); continue; }

        const tlDisplayName = displayNameFor(rawTL);
        let tlId = Object.entries(dataset.teamLeaders).find(([,n]) => normalize(n) === normalize(tlDisplayName))?.[0];
        if (!tlId) {
          tlId = 'tl_' + Math.random().toString(36).slice(2, 9);
          dataset.teamLeaders[tlId] = tlDisplayName;
        }
        dataset.assignments[uid] = tlId;
        matched++;
      }

      saveStored();
      render();
      const uniqueUnmatched = [...new Set(unmatched)];
      const shown = uniqueUnmatched.slice(0, 12).join(', ');
      const more = uniqueUnmatched.length > 12 ? `, +${uniqueUnmatched.length - 12} more` : '';
      const msg = uniqueUnmatched.length
        ? `Mapped ${matched} counselor(s) currently in this dataset.\n\n${uniqueUnmatched.length} name(s) in the mapping file aren't in the current call data (expected if the mapping covers more people than this dump), including: ${shown}${more}.`
        : `Mapped ${matched} counselor(s) to their team leaders.`;
      alert(msg);
    },
    error: (err) => {
      console.error('Parse error', err);
      alert('Could not read that file.');
    }

  });
}

function handleFile(file) {
  Papa.parse(file, {
    header: true,
    skipEmptyLines: true,
    complete: (results) => {
      const prevTeamLeaders = dataset ? dataset.teamLeaders : {};
      const prevAssignments = dataset ? dataset.assignments : {};
      dataset = aggregateRaw(results.data);
      dataset.teamLeaders = { ...prevTeamLeaders };
      dataset.assignments = { ...prevAssignments };
      filterUser = 'all'; filterDate = 'all'; filterTL = 'all';
      saveStored();
      render();
    },
    error: (err) => {
      console.error('Parse error', err);
      alert('Could not read that file. Make sure it is the call-detail CSV export.');
    }
  });
}

function tlFilteredRecords() {
  if (filterTL === 'all') return dataset.records;
  const memberIds = new Set(Object.entries(dataset.assignments).filter(([,tl]) => tl === filterTL).map(([uid]) => uid));
  return dataset.records.filter(r => memberIds.has(r.userId));
}

function openManageModal() {
  showManageModal = true;
  render();
}

function closeManageModal() {
  showManageModal = false;
  render();
}

function renderManageModal() {
  if (!showManageModal) return '';
  const tlEntries = Object.entries(dataset.teamLeaders);
  return `
    <div class="modal-backdrop" id="manage-backdrop">
      <div class="modal">
        <h2>Team leaders</h2>
        <p class="sub">Add TLs and assign each rep to one. Used to filter the dashboard by team.</p>
        <div class="tl-add-row">
          <input type="text" id="new-tl-name" placeholder="New team leader name">
          <button class="manage-btn" id="add-tl-btn">Add</button>
        </div>
        ${Object.entries(dataset.users).sort((a,b) => a[1].localeCompare(b[1])).map(([uid, uname]) => `
          <div class="assign-row">
            <span class="name">${esc(uname)}</span>
            <select data-assign="${uid}">
              <option value="">Unassigned</option>
              ${tlEntries.map(([tid, tname]) => `<option value="${tid}" ${dataset.assignments[uid]===tid?'selected':''}>${esc(tname)}</option>`).join('')}
            </select>
          </div>
        `).join('')}
        <div class="modal-actions"><button id="close-manage">Done</button></div>
      </div>
    </div>
  `;
}

function wireManageModal() {
  const backdrop = document.getElementById('manage-backdrop');
  if (!backdrop) return;
  backdrop.addEventListener('click', (e) => { if (e.target === backdrop) closeManageModal(); });
  document.getElementById('add-tl-btn').addEventListener('click', () => {
    const input = document.getElementById('new-tl-name');
    const name = input.value.trim();
    if (!name) return;
    const id = 'tl_' + Math.random().toString(36).slice(2, 9);
    dataset.teamLeaders[id] = name;
    saveStored();
    render();
  });
  document.querySelectorAll('[data-assign]').forEach(sel => {
    sel.addEventListener('change', () => {
      const uid = sel.dataset.assign;
      if (sel.value) dataset.assignments[uid] = sel.value;
      else delete dataset.assignments[uid];
      saveStored();
      render();
    });
  });
  document.getElementById('close-manage').addEventListener('click', closeManageModal);
}

(async function init() {
  await loadStored();
  render();
})();
</script>
</body>
</html>
