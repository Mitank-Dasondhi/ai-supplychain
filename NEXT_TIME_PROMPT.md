# Message to give to a new Claude or Grok

Copy everything below the line and paste it into a new chat. Then attach the files `index.html`, `data.csv` and `key.csv` (or paste them), and finish the last section.

---

I need help improving a small website that I host for free on GitHub Pages. I am not a developer. Please explain things in plain words, avoid jargon, and give me complete files I can copy and upload, not small pieces of code.

## What the project is

A tracker of companies in the AI supply chain, from energy and chips to data centers, AI models and apps. It was built from a Google Sheet called "AI Impact Tracker". It shows a directory with search and filters, an analytics tab with charts, a README tab and a Sources tab.

India and Outside India are always kept separate. Never mix them in a count, chart or list.

## The files

- `index.html`: the whole website in one file (page, styles and code). It has no outside libraries and no build step.
- `data.csv`: the company list. One row per company, with these columns in this order: Region, S.No, Company, Layer, Type, Supply chain level, Company kind, HQ, Country, City, Where they operate, What they make or do, Sells to, What happened, How sure, Latest update, Source, Last updated.
- `key.csv`: plain meanings of the labels (columns: Item, Kind, Plain meaning). It is optional and is shown on the README tab.
- `README.md`: instructions for me.

## How it works

- `index.html` reads `data.csv` and `key.csv` when it opens. **No company data is written inside `index.html`. Please keep it that way.**
- Settings I may change are in a block called `CONFIG` at the top of the script.
- Each value in the Region column becomes a button at the top (today: India and Outside India). Each region has four tabs: Companies, Analytics, README, Sources.
- The Companies tab has a search box, a Filters panel, clickable count tiles, filter chips, a sortable table, and rows that open to show every field.
- The Analytics tab has a donut and bars for the share of companies by layer, confidence in the news by layer, company kind, type, recent events, countries, cities and supply chain level. Clicking a bar opens those companies.
- Layers: 1 Energy, 2 Chips, 3 Infrastructure, 4 Models, 5 Applications.
- "How sure" values are Confirmed, Planned, Unconfirmed and `-` (shown as "No recent event").
- The "What happened" and "Country" columns can hold several values separated by commas. A company counts once in each.
- The page works in light and dark mode and on phones.

## Rules for any change

1. Keep reading the data from `data.csv`. Do not hard-code company data in the page.
2. Keep the column names exactly as they are, unless I ask you to change them. If you change them, also tell me what to change in my sheet and in `README.md`.
3. Keep the same look and the same features unless I ask otherwise.
4. Do not add outside libraries or anything that needs installing.
5. The page must still work when opened from GitHub Pages, and must show a clear message if `data.csv` cannot be loaded.
6. Test with all rows in `data.csv` (285 companies today: 185 India and 100 Outside India). Tell me the counts you see.
7. Give me the full new file for anything you change, and tell me in plain words which file to replace and how to upload it on GitHub.
8. If something in my request is unclear or could break the data, ask me one short question first.

## What I want to do next

(Write your request here in your own words. For example: "Add a map", "Add a column called Funding", "Make the table show 50 rows at a time", or "Change the colours".)
