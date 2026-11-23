# Indian Railways Commercial Analytics & Fare Engine (Excel)

A relational data-stitching and automated ticketing model built in Microsoft Excel using lookup functions (`VLOOKUP`, `HLOOKUP`, `XLOOKUP`, `INDEX` + `MATCH`) to integrate disconnected railway timetables, station directories, rate cards, and PNR booking registers.

## Project Files
- **`Indian_Railways_Lookup_Assignment.xlsx`**: Starter workbook featuring four unjoined master/transaction tables (`Train_Master` with 40 trains, `Station_Master` with 28 stations, `Rate_Cards` with 3 horizontal/vertical pricing & grading tables, and `Bookings` with 25 PNR records) alongside 5 structured analytical modules (`Q1`–`Q5`).
- **`Indian_Railways_Lookup_Assignment_Solved.xlsx`**: Completed workbook containing fully dynamic, formula-driven solutions across all 5 modules and the integrated fare calculation engine.

## Key Implementations & Modules
- **Q1 — `VLOOKUP` & Error Handling**: Extracted train attributes (`Train_Type`, `Distance_KM`, `Punctuality_Pct`), handled missing train IDs cleanly with `IFERROR`, compared route distances using `MAX` + nested `VLOOKUP`, and graded train punctuality via approximate-match slab lookups.
- **Q2 — `HLOOKUP` & Distance Slabs**: Queried horizontal fare matrices by travel class and train type, and computed distance-based reservation charges using ascending approximate-match thresholds.
- **Q3 — `XLOOKUP` & Dynamic Arrays**: Performed reverse (leftward) lookups from `Train_Name` to `Train_No`, spilled multi-column origin/destination station codes (`From_Code`, `To_Code`), retrieved the latest PNR booking via reverse search (`search_mode = -1`), and resolved full destination station names using nested `XLOOKUP`s.
- **Q4 — `INDEX` + `MATCH` & Multi-Criteria Lookups**: Executed two-way row/column matrix lookups on `Rate_Cards`, identified extreme operational metrics (`MAX` distance and worst average delay), and performed multi-criteria array lookups (`From_Code` + `Train_Type`) resilient to column insertions.
- **Q5 — Integrated Fare Register (`Bookings`)**: Automated 8 derived columns (`Train_Name`, `Train_Type`, `Distance_KM`, `Rate_per_KM`, `Reservation_Charge`, `Total_Fare`, `Boarding_City`, and `PREMIUM`/`STANDARD` tier flags) across 25 PNR transactions.

## Analytical Highlights & KPIs
- **Total Booking Revenue**: **₹70,610** collected across 25 PNR bookings (July 2–14, 2026).
- **Highest-Value Booking**: **PNR100261** (1A class on *12213 Yesvantpur Duronto Express*, 2,364 km) generated the highest single-ticket fare at **₹10,029**.
- **Premium Tier Split**: 5 bookings exceeded ₹4,000 and were automatically flagged as `PREMIUM`, while 20 bookings fell into the `STANDARD` tier.
- **Fleet & Service Insights**: 4 bookings were made on *Vande Bharat* services; *Trivandrum Rajdhani Express* covered the longest route (3,149 km), while *Kamrup Express* recorded the highest average delay.

## Tools & Excel Functions Used
- **Lookup & Reference**: `VLOOKUP` (Exact & Approximate), `HLOOKUP`, `XLOOKUP` (reverse search, dynamic spill, `if_not_found`), `INDEX` + `MATCH` (two-way & multi-criteria)
- **Logic, Math & Aggregation**: `IF`, `IFERROR`, `ROUND`, `MAX`, `SUM`, `COUNTIF`
