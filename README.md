# Why Did Medicare Payment per Discharge Rise? A Price and Mix Analysis of Massachusetts Hospitals, 2019 to 2021

An Excel analysis that splits the increase in average Medicare payment per hospital discharge into two causes: a change in the mix of conditions treated, and a change in the price paid for the same condition.

**Tools:** Excel (pivot table, linked formulas, waterfall and bar charts)
**Data:** CMS Medicare Inpatient Hospitals by Provider and Service, Massachusetts, 2019 and 2021 (55 hospitals, 435 DRGs, 10,055 rows). [ADD THE CMS DATA LINK HERE]
**Files:** `ma-medicare-price-mix-analysis.xlsx` (full workbook), `images/` (charts)

## The question
Average Medicare payment per discharge in Massachusetts hospitals went up between 2019 and 2021. Was that because hospitals were paid more for the same care, or because they were treating a different, more expensive mix of patients?

## Result

| | Value |
|---|---|
| Average payment per discharge, 2019 | $16,075 |
| Average payment per discharge, 2021 | $18,315 |
| **Total change** | **+$2,240 (+13.9%)** |
| Mix effect | +$734 (33% of the change) |
| Price effect | +$1,506 (67% of the change) |

**About two-thirds of the increase came from higher payments for the same type of case, and one-third came from a shift in which cases hospitals treated.**

## What drove it
- **Biggest mix increase:** respiratory infections with major complications (DRG 177), adding about $586 per discharge, followed by endovascular cardiac valve replacement (DRG 267, about $92).
- **Biggest mix decrease:** major hip and knee joint replacement (DRG 470), about $426 per discharge, a lower-cost elective procedure that became a smaller share of cases.
- **Biggest price increases:** DRG 177 again (about $216 per discharge), then sepsis (DRG 871, about $112) and ECMO or tracheostomy cases (DRG 3, about $76).
- 2021 falls in the COVID-19 pandemic, which may explain the rise in respiratory cases and the drop in elective surgery. The data shows the shift, but it does not prove the cause.

## Method
1. Built a pivot table of discharges and total payment (average payment x discharges) by DRG and year.
2. For each DRG, calculated its **average payment** and its **share of all discharges** in each year.
3. Calculated for each DRG:
   - **Mix effect** = (2021 share - 2019 share) x 2019 average payment
   - **Price effect** = 2021 share x (2021 average payment - 2019 average payment)
4. Summed across DRGs. The two effects add up exactly to the total change, which the workbook checks.
5. Charted the result as a waterfall, and the top and bottom 10 DRGs for each effect as bar charts.

## Limitations
- Only the **362 DRGs present in both years** are included, out of 435 in the data.
- Payments are **not adjusted for inflation**, and the "price effect" is the change in average payment for the same DRG. It includes Medicare rate updates and differences between hospitals, not only a pure price change.
- Medicare patients only, Massachusetts only, and two years only (2020 is not included).
- Small-volume DRGs may be missing from the CMS data.

## What I did
Individual project. I built the pivot table, the price and mix calculations, the summary table and the charts, and wrote the conclusions.
