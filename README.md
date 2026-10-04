# SAMA POS Analysis — Q1 vs Q2 2026

**Zahrah Faleh Al-Odhaylah · R · Statistical Analysis**

[Report](https://zahrah-002.github.io/sama-pos-2026/) · [Code](SAMA_Report.Rmd) · [Dataset](SAMA_Sales_2026.xlsx) · [Build status](https://github.com/zahrah-002/sama-pos-2026/actions)

## Overview

A comparison of point-of-sale activity across 27 aggregated items in the supplied Saudi Central Bank (SAMA) dataset. The analysis examines transaction count, transaction value, average transaction value (ATV), and item-level changes between Q1 and Q2 2026.

## Analytical Questions

- How did total transaction count and value change?
- Which items recorded the largest increases and declines?
- How did ATV change?
- How do transaction volume and ATV contribute arithmetically to the value change?

## Methodology

1. Import and validate the Excel data: required columns, year, missing values, and duplicate items.
2. Reconcile item totals with source totals.
3. Calculate quarterly differences, growth rates, shares, and ATV.
4. Summarize item distributions and perform exploratory paired statistical comparisons.
5. Visualize selected items and overall transaction value; export results to Excel.

## Units

| Measure | Source unit | Presentation unit |
| --- | --- | --- |
| Transaction count | Thousand transactions | Million transactions |
| Transaction value | Thousand SAR | Billion SAR |
| Average transaction value | Value divided by count | SAR per transaction |

Overall ATV is calculated as total value divided by total count.

## Project Files

| File | Purpose |
| --- | --- |
| [SAMA_Report.Rmd](SAMA_Report.Rmd) | Analysis code, narrative, tables, and charts |
| [SAMA_Sales_2026.xlsx](SAMA_Sales_2026.xlsx) | Input workbook: Clean_Data and Source_Totals |
| [.github/workflows/pages.yml](.github/workflows/pages.yml) | Builds the report and deploys it to GitHub Pages |

Rendering creates an Excel results workbook and chart images inside `SAMA_2026_Project/`. The publishing workflow includes these outputs under the site's `results/` folder.

## Run the Analysis

Place the R Markdown file and Excel input in the same folder. Run in R:

```r
install.packages(c("rmarkdown", "knitr", "readxl", "dplyr",
                   "tidyr", "ggplot2", "writexl"))
rmarkdown::render("SAMA_Report.Rmd", output_file = "index.html")
```

Rendering requires Pandoc, which is included with RStudio. For hosted builds, check Actions to confirm the latest deployment succeeded.

## Interpretation

These are aggregated quarterly observations. Statistical comparisons across items are exploratory and do not establish causality or changes in individual consumer preferences. The volume/ATV decomposition is arithmetic. Geographic coverage should be confirmed from the original source export.

---

<div dir="rtl" lang="ar">
<h2>عن المشروع</h2>
<p>تحليل بيانات نقاط البيع للربع الأول والثاني من عام 2026 باستخدام R، لمقارنة عدد العمليات وقيمتها ومتوسط قيمة العملية عبر 27 بندًا مجمّعًا في ملف بيانات البنك المركزي السعودي (ساما).</p>
<p>يشمل التحقق من البيانات ومطابقة الإجماليات، وحساب التغير ونسب النمو، وتحليل البنود، والإحصاءات الوصفية والمقارنات الاستكشافية، وعرض الرسوم وتصدير النتائج إلى Excel.</p>
<p>تُعرض أعداد العمليات بالمليون، والقيم بمليار ريال، ومتوسط قيمة العملية بالريال. وتُفسّر النتائج ضمن حدود البيانات المجمّعة المتاحة.</p>
</div>
