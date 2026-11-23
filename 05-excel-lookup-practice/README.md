# Excel Lookup Functions & Reference Mechanics Practice

A hands-on Excel workbook covering core vertical, horizontal, two-way, and range-based lookup techniques alongside relative, absolute, and mixed cell referencing across six structured business and academic datasets.

## Project Files
- **`Lookup_Practice.xlsx`**: Starter practice workbook containing a `README` guide and 6 interactive lookup exercises with worked examples and dynamic input zones.
- **`Copy of Classroom Assignment - Lookup All.xlsx`**: Completed workbook featuring custom lookup queries, `XLOOKUP` implementations, multi-parameter test cases, and cell-referencing demonstrations (`D5`, `$D$5`, `$D5`/`D$5`).

## Workbook Modules & Lookup Implementations
1. **`1. Employee-Dept` (Relational & Nested Lookups)**: Joined an 8-employee directory (`EmpID` `101`–`108`) with a 4-department table (`D1`–`D4`) using `VLOOKUP`, nested `VLOOKUP`, and `INDEX` + `MATCH` to dynamically retrieve employee names, department IDs, department names, and managers (`105` → *Kabir Nair*, Finance, *M. Joshi*; `106` → *Ishaan Gupta*, Sales, *R. Banerjee*).
2. **`2. Product Price` (Exact-Match & Fallback Handling)**: Queried an 8-item product catalog (`P001`–`P008`) using `VLOOKUP` and `XLOOKUP` (with custom `if_not_found` fallback handling) to fetch item names, prices, categories, and stock levels (`P004` → *27in Monitor*, ₹18,999; `P007` → *Noise-Cancel Headset*, ₹5,999).
3. **`3. Student Grades` (Two-Way Matrix Lookup)**: Implemented `INDEX` + `MATCH` + `MATCH` across a 6-student × 5-subject grade matrix to pull intersectional scores (*Ananya* in *Chemistry* = `59`; *Diya* in *Math* = `59`) alongside subject-level class averages (`70.17`).
4. **`4. Sales Grid` (Horizontal & Cross-Tab Aggregations)**: Combined `HLOOKUP`, `INDEX` + `MATCH` + `MATCH`, and `HLOOKUP` + `SUM` across a 5-region × 6-month revenue grid (`Jan`–`Jun`) to extract regional monthly figures (*Central* in *Apr* = `43,000`; *West* in *Mar* = `161,000`) and monthly totals (*Mar* = `848,000`).
5. **`5. Exam Timetable` (Schedule Grid Lookup)**: Used `HLOOKUP` and two-way `INDEX` + `MATCH` across a weekday × period timetable (`Mon`–`Fri`, `P1`–`P4`) to retrieve scheduled subjects (*Wed*, Period 3 = *Math*; *Mon*, Period 2 = *Physics*).
6. **`6. Price Bands` (Approximate-Match Tiering)**: Applied range-based `VLOOKUP(..., TRUE)` on an ascending spend-threshold table (`₹0` to `₹25,000+`) to assign discount percentages, loyalty tiers, and discount amounts (`₹7,500` spend → `10%` *Silver* tier, `₹750` discount).

## Tools & Excel Functions Used
- **Lookup Functions**: `VLOOKUP` (Exact & Approximate Match), `HLOOKUP`, `XLOOKUP` (with `if_not_found`), `INDEX` + `MATCH` (Single & Two-Way)
- **Supporting Functions & Concepts**: `SUM`, `AVERAGE`, nested lookups, Relative (`D5`), Absolute (`$D$5`), and Mixed (`$D5` / `D$5`) cell referencing
