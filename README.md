# AI Impact Tracker

## What this is

This is a small website that shows a list of companies in the AI supply chain, from energy and chips to data centers, AI models and apps.

You can search the list, filter it, click a company to read its latest update and source, and see charts. The companies are split into two groups that are never mixed: **India** and **Outside India**.

The website has four parts for each group: **Companies**, **Analytics**, **README** and **Sources**.

## Where the data came from

All the data comes from one Google Sheet called **AI Impact Tracker**. It has two tabs of companies (India and Outside India) and a Key tab that explains the labels.

The data was copied out of that sheet on 12 November 2026. It has 285 companies: 185 in India and 100 Outside India.

## What is in this folder

| File | What it does |
|---|---|
| `index.html` | The website itself. You never need to change it. |
| `data.csv` | **The company list. This is the only file you replace when you update.** |
| `key.csv` | The plain meanings of the labels (layers, types and so on). It is shown on the README tab. Optional. |
| `README.md` | This page. |
| `NEXT_TIME_PROMPT.md` | A message you can give to an AI helper later to keep improving the project. |

The website reads `data.csv` every time it opens. No company is written inside `index.html`.

## How to update the data later

You only replace one file: `data.csv`.

### Step 1. Make one combined sheet in Google Sheets

The Google Sheet keeps India and Outside India on separate tabs, but `data.csv` needs one list with a **Region** column.

1. Open your Google Sheet.
2. Click the **+** at the bottom left to add a new empty tab. Name it **Export**.
3. Go to the **India** tab. Click the small square at the top left of the grid to select everything, then press Ctrl+C (Cmd+C on Mac).
4. Go to the **Export** tab. Click cell **B1**. Press Ctrl+V (Cmd+V). The header row and all India companies are now in the Export tab, starting in column B.
5. Go to the **Outside India** tab. Select everything except the first row (the header). Copy it.
6. In the Export tab, click the first empty cell in column B, right under the last India company. Paste.
7. In cell **A1**, type `Region`.
8. In column A, next to every India company type `India`. Next to every Outside India company type `Outside India`. (Type it in the first cell, then drag the little square at the corner of the cell down to fill the rest.)

### Step 2. Check these things

- The first row has the column names, spelled exactly as before: `Region`, `S.No`, `Company`, `Layer`, `Type`, `Supply chain level`, `Company kind`, `HQ`, `Country`, `City`, `Where they operate`, `What they make or do`, `Sells to`, `What happened`, `How sure`, `Latest update`, `Source`, `Last updated`.
- **Do not rename, remove or add header names.** If you must add a new column, ask an AI helper to update the website first.
- **No merged cells.**
- **No empty rows** in the middle of the list.
- Every row has a **Company** name and a **Region**.
- Write dates like `2026-11-12` (year, month, day).
- Leave `How sure` as `-` when there is no recent event.
- A new Region name (for example `Middle East`) automatically gets its own button on the website.

### Step 3. Save it as a CSV file

1. In Google Sheets, make sure the **Export** tab is open.
2. Click **File**, then **Download**, then **Comma Separated Values (.csv)**.
3. A file downloads. Rename it to exactly **data.csv**.

(If you use Excel instead, choose **Save As** and pick **CSV UTF-8 (Comma delimited)**.)

### Step 4. Replace the file on GitHub

1. Open your repository on GitHub.
2. Click **Add file**, then **Upload files**.
3. Drag your new `data.csv` into the box. It has the same name, so it replaces the old one.
4. Scroll down and click the green **Commit changes** button.
5. Wait 1 to 2 minutes, open your website link, and press **Ctrl+F5** (Cmd+Shift+R on Mac) to see the new data.

## If something looks wrong

- **The page says "Open this page from its web link".** You double-clicked `index.html` on your computer. Open your GitHub link instead.
- **The page says it could not find data.csv.** Check the file is in the same folder as `index.html` and is named exactly `data.csv` (small letters).
- **The page says column names are missing.** The first row of `data.csv` has a changed or misspelled column name. Compare it with the list above.
- **You still see the old data.** Wait a minute or two, then do a hard refresh (Ctrl+F5, or Cmd+Shift+R on Mac).
- **Some labels look odd or accents look broken.** Save the file again as **CSV UTF-8**.

## Who can see this site

A free GitHub site is public. Anyone who has the link can open it, and the `data.csv` file is public too. Only put in data you are happy to share.
