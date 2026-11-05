<p align="center"><img src="assets/banner.svg" alt="HR Timekeeping Portal" width="100%"></p>

<p align="center">
<img src="https://img.shields.io/badge/stack-Apps_Script_·_HTML_Service_·_Sheets-5B3A3A?style=flat-square">
<img src="https://img.shields.io/badge/data-fictional-FBE3EC?style=flat-square">
<a href="https://sider.ai/agents/web-creator/share/695ea81100a621619985fdfb"><img src="https://img.shields.io/badge/Portfolio-Nae_Kitakado-F4B4CD?style=flat-square"></a>
</p>

<p align="center"><a href="https://naekitakadoportfolio.github.io/hr-timekeeping-portal/"><img src="https://img.shields.io/badge/%E2%96%B6%20Try%20the%20live%20demo-5B3A3A?style=for-the-badge" alt="Live demo"></a></p>

# HR Timekeeping Portal

A timekeeping and payroll-support portal for remote contractors. Clock in and out, submit a correction, then switch to Timekeeper or HR to approve it and watch the payslip update.

> **Portfolio rebuild.** This is a from-scratch recreation of a production system I designed and run, rebuilt with **fictional data** and no client names, code or branding. The live demo runs entirely in the browser.

## The problem
A remote contractor team tracked time in a paid time tracker that didn't handle local leave policy, hourly contractors in other countries, or payroll and invoicing support.

## Impact in production
Built a lightweight portal to replace the paid tool: clock-in/out, corrections with approval, leave by policy, payslip and invoice support, and HR, Timekeeper and Admin roles. It was designed so ownership can be handed to HR later, with data fully separate from other systems.

## What it demonstrates
| Capability | How |
|---|---|
| Self-service time tracking | Clock in/out with live shift state |
| Approval workflow | Corrections routed to Timekeeper or HR |
| Role-based access | Employee, Timekeeper, HR and Admin Manager |
| Payroll support | Approved hours × rate → payslip/invoice |
| Data migration | CSV upload of historical leave usage |

## Production architecture
Apps Script web app (HTML Service) · Sheets as data store · role table · CSV import · light/dark themed UI · designed for ownership handover

## Try it
Open the **[live demo](https://naekitakadoportfolio.github.io/hr-timekeeping-portal/)** or run `index.html` locally. No install needed.

---
<p align="center"><sub>Built by <b>Nae Kitakado</b>, AI Automation Consultant · <a href="https://www.linkedin.com/in/nae-k-203194265">LinkedIn</a> · <a href="https://sider.ai/agents/web-creator/share/695ea81100a621619985fdfb">Portfolio</a> · open to retainer &amp; part-time consulting</sub></p>
