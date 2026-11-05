<p align="center"><img src="assets/banner.svg" alt="HR Timekeeping Portal" width="100%"></p>

<p align="center">
<img src="https://img.shields.io/badge/stack-Apps_Script_·_HTML_Service_·_Sheets-0F2A44?style=flat-square">
<img src="https://img.shields.io/badge/data-fictional-C0C8D2?style=flat-square">
<a href="https://sider.ai/agents/web-creator/share/695ea81100a621619985fdfb"><img src="https://img.shields.io/badge/Portfolio-Nae_Kitakado-0F2A44?style=flat-square"></a>
</p>

<p align="center"><a href="https://naekitakadoportfolio.github.io/hr-timekeeping-portal/"><img src="https://img.shields.io/badge/%E2%96%B6%20Try%20the%20live%20demo-0F2A44?style=for-the-badge" alt="Live demo"></a></p>

# HR Timekeeping Portal

A timekeeping and payroll-support portal for remote contractors: live time clock with breaks, cutoff timesheets, corrections and leave with approvals, policy-based balances, payroll and payslips in multiple currencies, CSV exports, people and role management, and historical leave imports.

> **Portfolio rebuild.** A from-scratch recreation of a lightweight HR portal built to replace a paid time tracker for a remote contractor team, a production system I designed. It uses **fictional data**, with no client names, code or branding.

## ✨ Features
- **Dashboard:** hours this cutoff, leave left, who's on shift, items to approve and the cutoff payroll total
- **Time clock:** clock in/out with a live timer and breaks (demo speed: 1 s = 1 min)
- **Timesheets:** calendar grid per semi-monthly cutoff, approved hours, leave overlay, submit for review, request corrections
- **Approvals:** Timekeeper approves time corrections; HR approves leave with balance-after shown
- **Leave:** requests validated against policy balances, plus a month calendar of team leave
- **Payroll & payslips:** hourly and fixed contractors, USD/PHP/PKR display, payslip modal, invoice CSV export (file download)
- **People & roles:** HR/Admin edit roles and rates and add contractors (country-specific leave policy)
- **Imports:** paste historical leave CSV → row-level validation preview → apply valid rows
- **Activity:** full audit trail
- **Light/dark theme**, responsive layout, state saved in your browser, and a one-click demo reset

## 🧭 Try it
1. As **Ava Reyes**, clock in, take a break, clock out
2. Open *Timesheets* → **Request correction**
3. Switch to **Tina Go** (Timekeeper) → *Approvals* → approve
4. Switch to **Hana Sy** (HR) → *Payroll* → change currency → **Export invoice CSV**

Open the **[live demo](https://naekitakadoportfolio.github.io/hr-timekeeping-portal/)**.

## 🏗 Production architecture
| Layer | Production | This demo |
|---|---|---|
| UI | Apps Script HTML Service web app | Static SPA (`index.html`) |
| Data | Google Sheets (shifts, leave, people) | `localStorage` |
| Roles | Role table keyed by Google account | Signed-in-as switcher |
| Exports | Sheet export / Drive CSV | Blob download |
| Imports | CSV upload to staging sheet | Paste → preview → apply |

## 📁 Project structure
```
hr-timekeeping-portal/
├── index.html        # built app (shell + app code)
├── src/app.js        # views, state and business logic
├── src/app.json      # navigation, theme and build config
├── assets/banner.svg
├── README.md
└── LICENSE
```

## 🚀 Run locally
No build step needed. Open `index.html` in a browser, or serve it:
```bash
python3 -m http.server 8000   # then visit http://localhost:8000
```

## 🧩 Key implementation notes
- `hours()` sums approved shifts inside the selected cutoff
- `gross()` pays hourly contractors on approved hours and fixed contractors half-monthly
- Corrections become approved shifts only after Timekeeper approval
- Imports validate the person, leave type and date format before anything is written

## 🗺 Roadmap
- Overtime and night-differential rules
- Holiday calendar per country
- Bulk payslip PDF export

---
<p align="center"><sub>Built by <b>Nae Kitakado</b>, AI Automation Consultant · <a href="https://www.linkedin.com/in/nae-k-203194265">LinkedIn</a> · <a href="https://sider.ai/agents/web-creator/share/695ea81100a621619985fdfb">Portfolio</a> · open to retainer &amp; part-time consulting</sub></p>
