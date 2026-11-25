# Data Stock & Margin Assistant

A stock and reorder tool for food wholesalers: what to reorder every morning, and a record of the stock every day.

**Try it:** open the live page (GitHub Pages link at the top right of this repository, under *About*).

Capstone project, Group 2, Section 1 · *Human & AI Collaboration for Logistics* · KEDGE Business School · November 2026
Martin Ales, Amandine Brezault, Emile Delhoye, Jesse Nicolas, Chamseddine Sliti, Carla Vannieri

## What it does

The tool has one window per function:

1. **Today's files** – the 9:00 routine: the stock file and the sales and margins (audit) file arrive by email, are saved to SharePoint and read by the tool. Files can also be added by hand (Excel or CSV).
2. **Columns** – any Excel file works: the column names are matched to the fields the tool needs (article, stock, date, quantity sold…) and confirmed once by a person.
3. **What to reorder** – days of cover = (stock + quantity on order) ÷ sales per day over 12 months. Reorder now when it is at or below the supplier lead time + 15 days of safety.
4. **Stock history** – the stock of every article is recorded each day; lines are only added and a day is never written twice.
5. **Rules** and 6. **The standard** – the settings of the calculation and the file format every source must follow.

Everything runs in the browser: files are read on your computer and are not uploaded anywhere.

## Test data

The page opens on **Northwind Traders**, Microsoft's public sample database of a fictional food importer (77 products, 2,155 order lines, 1996–1998). The mailbox and SharePoint are simulated. The 30-day stock history uses the real Northwind order lines with a simulated opening stock and supplier receipts. The Excel files are in the `data` folder and can be loaded with *Add today's files by hand*.

## Use of AI

The tool was built with the help of Claude (Anthropic). Inside the tool, AI is used only to suggest the column match, and it sees only the column names, never the data. That suggestion works in the Claude-hosted version of the tool; on this public page the columns are matched by name and confirmed by the user. All calculations are plain code.
