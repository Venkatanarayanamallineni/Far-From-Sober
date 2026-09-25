

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Georgia&size=32&duration=3500&pause=1200&color=F1BE48&center=true&vCenter=true&width=700&lines=Far+From+Sober;Ames%2C+Iowa+%C2%B7+2018%E2%80%932026;COVID+Growth+%C3%97+Cyclone+Gamedays" alt="Typing SVG" />

<br>

### How a college town's liquor sales survived lockdown and learned to love kickoff

<br>

[![Live Dashboard](https://img.shields.io/badge/▶_Live_Interactive_Dashboard-8C1D40?style=for-the-badge&logo=tableau&logoColor=F1BE48)](https://public.tableau.com/views/IowaLiquorSalesCOVIDImpactGamedayTrendsAmes/Amesstory?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

</div>

<br>

<div align="center">
<img src="https://img.shields.io/badge/Tableau-E97627?style=flat-square&logo=tableau&logoColor=white" />
<img src="https://img.shields.io/badge/Power_BI-F2C811?style=flat-square&logo=powerbi&logoColor=black" />
<img src="https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white" />
<img src="https://img.shields.io/badge/DAX-217346?style=flat-square&logo=microsoftexcel&logoColor=white" />
<img src="https://img.shields.io/badge/Excel_Power_Query-217346?style=flat-square&logo=microsoftexcel&logoColor=white" />
</div>

---

## The Question

Did liquor sales in Ames, Iowa actually change through COVID — and does Iowa State football gameday activity move the needle? This project analyzes roughly **4 million transactions** (2018–2026), filtered to Ames city, split into Pre-COVID, COVID, and Post-COVID periods, to find out.

**Data sources:**
- [Iowa Liquor Sales](https://data.iowa.gov) — public wholesale distribution records (official year-wise pulls + Kaggle extract)
- Iowa State Cyclones football schedule (2018–2026) — compiled from [cyclones.com](https://cyclones.com) and [Sports Reference](https://www.sports-reference.com/cfb/schools/iowa-state/)

---

## 📈 Key Findings

<div align="center">
<img src="https://img.shields.io/badge/Pre--COVID-$5.39M-1A1613?style=for-the-badge" />
<img src="https://img.shields.io/badge/→-F1BE48?style=for-the-badge" />
<img src="https://img.shields.io/badge/COVID_Era-$9.60M_(+78%25)-8C1D40?style=for-the-badge" />
<img src="https://img.shields.io/badge/→-F1BE48?style=for-the-badge" />
<img src="https://img.shields.io/badge/Post--COVID-$18.93M_(+97%25)-F1BE48?style=for-the-badge&logoColor=black" />
</div>

<br>

**Sales nearly quadrupled, and growth *accelerated* rather than leveling off** — the second jump (COVID → Post-COVID) outpaced the first.

**Iowa is the top-grossing gameday matchup** — $2.86M in gameday-window sales across all tracked seasons, though the top rival shifted by era (Oklahoma, Texas Tech, and West Virginia briefly led during 2020's COVID-year home games).

**October is the seasonal peak — and 2025 broke the streak with fewer games.** Every season, October carries the highest gameday sales. 2025 topped 2024's high *despite having one fewer home game* — ruling out "more games = more sales" as the explanation.

**Win or lose, Ames still drinks — but recent wins pull ahead.** Gallons sold by game outcome were inconsistent early on (2022 saw Losses outsell Wins), but 2024–2025 show a clear shift toward Wins driving more volume.

---

## 🏈 Watching Now: October 2026

| | Home Games | Result |
|---|---|---|
| 2024 | 2 | Set the prior high |
| 2025 | 1 | Broke it anyway |
| **2026** | **2** | *In progress — Oct 3 vs West Virginia, Oct 31 vs Oklahoma State* |

Fewer games, higher sales in 2025 rules out "more football = more spending" as the whole story. New head coach, full October home slate — the dashboard will track whether 2026 keeps the streak alive.

---

## 🔍 Methodology

- Filtered Iowa's full statewide liquor dataset (34M+ rows) down to Ames city
- Built a Period calculated field (Pre-COVID / COVID / Post-COVID) using verified U.S. and Iowa COVID emergency declaration dates
- Joined transaction data to a compiled ISU football schedule using a ±3-day gameday window — source data has sparse daily coverage, so exact-date-only joins under-captured real gameday activity
- Verified every headline % change by hand against raw totals before trusting the tool's output
- Cross-validated totals in SQL (SQLite: joins, CTEs, window functions) — caught and fixed a duplicate-row join bug that had inflated one draft's totals by ~3.6x

> **Known limitation:** gameday/team-level splits use a thin sample (as few as 5–8 matched dates per opponent). These cuts are directional, not statistically robust — read them as a hypothesis for further study, not a precise estimate.

---

## 🛠️ Built With

<div align="center">
<img src="https://skillicons.dev/icons?i=powerbi&theme=dark" height="40" />
&nbsp;&nbsp;
<img src="https://img.shields.io/badge/-Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white" height="40"/>
</div>

Tableau (calculated fields, joins, dashboard & story design) · Power BI (DAX) · SQL (SQLite — joins, CTEs, window functions, CASE logic) · Excel / Power Query (data cleaning)

---

<div align="center">

[![Live Dashboard](https://img.shields.io/badge/▶_View_the_Full_Dashboard-8C1D40?style=for-the-badge&logo=tableau&logoColor=F1BE48)](https://public.tableau.com/views/IowaLiquorSalesCOVIDImpactGamedayTrendsAmes/Amesstory?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

Built by V — Iowa State University, Ivy College of Business

</div>
