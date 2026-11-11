# MRPilot — Inventory Optimization and MRP Planner

**Live demo:** https://YOUR-GITHUB-USERNAME.github.io/mrpilot

A working MRP and finite-scheduling tool built to SAP planning logic, on two sample products:
a smart thermostat (Dallas) and a city bike (Monterrey). Every visitor gets a private copy; nothing they change is shared.

## What it does
- **Control Tower (≈ MD06):** exception messages by item, worst first, with owner assignment
- **Supply Plan (≈ MD01 / MD04):** multi-level gross-to-net, lot sizing, firm zone, pegging, calendar weeks
- **Demand Planning (≈ MD61):** six forecast methods incl. seasonal, backtested, with forecast consumption
- **Inventory Policy:** ABC/XYZ, service-level safety stock, reorder point, min-max, periodic review
- **Capacity (≈ CM01 / CM21) and Scheduling (≈ CM25):** rough-cut load, leveling, finite scheduling with setups, labor, shifts, downtime, dispatch list
- **Purchasing (≈ ME51N / ME54N / ME21N / MIGO):** requisition, release by value limit, PO, goods receipt
- **Guided tour** that runs the planning cycle live: shortage → owner → requisition → release → PO

## How it was verified
- Every number is computed twice: by the web engine and by an Excel workbook of ~819,000 formulas. **2,404 parity checks, 0 mismatches**; a 480-item export matches on 29,069 checks.
- ~400 automated browser checks: planner workflows, multi-user, 20,000-item scale, UI on desktop/tablet/phone, random wear-and-tear sessions.

## Run it
Open `index.html` in a browser, or serve the folder with any static host (GitHub Pages, Netlify).
`engine_template.js` holds the Excel model and loads only when someone downloads Excel.

---
© 2026 Rohit Patil. All rights reserved. Demo data is fictional; company names are invented.
Made by Rohit Patil · MS Supply Chain Management, UT Dallas
