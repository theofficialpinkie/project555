# PlanReview — Pay Item Checker

AI-assisted bridge contract plan reviewer. Checks NYSDOT Section 555 pay item compliance using spatial coordinate analysis.

## What it does
- Upload any bridge plan PDF
- Detects missing pay item numbers using PyMuPDF-style spatial coordinate checks (runs client-side via PDF.js)
- Flags PROPOSED elements with no adjacent (ITEM NO.) callout
- Checks concrete tables for item number completeness
- Validates item numbers against NYSDOT Section 555 catalogue
- Works sheet by sheet or full plan set at once

## How to use
1. Open the app
2. Drop a PDF bridge plan
3. Click "Review this sheet" or "Review ALL sheets"
4. Red boxes highlight flagged elements on the drawing

## Tech
- Pure HTML/JS — no backend required
- PDF.js for client-side PDF rendering and text extraction
- Spatial adjacency check: flags PROPOSED elements with no (ITEM NO.) within 180 PDF points
- Vercel static deployment
