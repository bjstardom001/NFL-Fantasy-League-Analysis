
   # 🏈 Introduction
   This project offers an interactive analysis of NFL player and team performance from 1999 to 2013. Using Power BI, the dashboard highlights how player attributes, college conferences, draft data, and geographic origins influence NFL outcomes, including fantasy points, combine results, and long-term team success.

   # 📚 Background
   The NFL Draft and player development are strongly influenced by college programs, physical attributes, and regional pipelines. Evaluating which states, colleges, and conferences produce top players, and how rookies vs veterans contribute to team performance, helps uncover deeper insights into talent distribution.

**This analysis draws on:**

**•	Player-level data:** Fantasy points, draft picks, positions, physical combine metrics.

**•	College & Conference data:** Draft representation and player production.

**•	Team-level data:** Wins, losses, win percentage.

**•	Geographic data:** State and hometown representation.

# 🛠 Tools Used

**•	Power BI Desktop:** Data cleaning, modeling, visualization.

**•	Excel (Source File: NFL Statistics 1999–2013.xlsx):** Raw player, team, and geographic data.

**•	DAX (Data Analysis Expressions):** For calculated measures like rookie share, fantasy points, per capita player counts, and win rates.

**•	Geographic Mapping:** Filled maps for state-level and hometown analysis using zip/population data.

# 🧹 Data Cleaning & Preparation Process

In building my NFL Power BI dashboard, I carried out a thorough data cleaning and preprocessing stage using both Excel and Power Query to ensure data accuracy and consistency across all six tables in my dataset.

**1. Handling Missing Values:**
Some columns had missing entries (e.g., Wonderlic, Bench, Combine results).

***To maintain accuracy:***

I identified these missing values.

For cases where 0 appeared but was not a valid NFL measurement (like Wonderlic score = 0 or Bench reps = 0), I replaced those with null (none).

This ensured that averages were not artificially pulled down by placeholder zeros.

 **2. Correcting Lookup & Data Type Issues**
I had six interlinked tables, some originally joined via Excel VLOOKUPs.

***Problems discovered:***

Mismatched data types (e.g., text vs number) caused incorrect lookups.

Incorrect formulas returned wrong values.

***Fix:***

Standardize data types across all tables before merging.

Corrected VLOOKUP issues to ensure accurate referencing between player, team, and conference data.

**3. Removing Duplicates**

Detected duplicate player rows that appeared in multiple tables.

Removed these duplicates to avoid over-counting players in my totals and distinct measures.

**4. Eliminating Irrelevant Tables**
***Out of the six tables:***

Two (player name/conference, team name/conference mapping) were not essential for the final analysis.

These were dropped to simplify the data model.

 **5. Validating Data Accuracy**
 
Used Power Query profiling tools to check column distributions.

***Applied histograms to confirm data spread and consistency:***

Verified that cleaned values aligned with expected NFL ranges (e.g., Wonderlic ≈ 20–25, 40yd ≈ 4–6s).

Ensured there were no anomalous spikes caused by placeholder values.

**6. Data Modeling in Power BI**

Loaded the cleaned tables into Power BI.

Built relationships across tables (Player–Team–Conference–Combine–Stats).

Ensured relational integrity so slicers, filters, and visuals could cross-filter correctly.

# ✅ Impact of Cleaning on Analysis
**This cleaning process directly improved the accuracy of insights:**

Average metrics (Wonderlic, Bench, 40yd) reflected true performance instead of being skewed by invalid zero values.

Player counts (Total, Distinct, Rookie vs Veteran) became consistent across visuals, avoiding double counting.

Conference and geographic analyses became more reliable because lookup mismatches were resolved.

The final Power BI data model was leaner (only relevant tables kept), which improved performance and usability.

# The Analysis 


**1) Key numbers (from your uploaded dashboard)**

```
-Distinct players:
~2,000.

-Total fantasy points (all players):
~135,000.

-Average fantasy pts per player: 67.5 (calculated = 135,000 ÷ 2,000). 


-Average age:

27.04; Avg games per player: 11.45. 



-Top 10 players by fantasy points (from the dashboard): 
LaDainian Tomlinson (RB) 427; Peyton Manning (QB) 410; Tom Brady (QB) 398; Aaron Rodgers (QB) 397; Drew Brees (QB) 396; Daunte Culpepper (QB) 381; Marshall Faulk (RB) 381; Cam Newton (QB) 373; Priest Holmes (RB) 373; Shaun Alexander (RB) 364. (Top10 skew → 6 QBs / 4 RBs). 



-Combine metric averages:
Avg 40yd ≈ 4.80s, Avg Bench ≈ 21.34 reps, Avg Wonderlic shown as 25.69. 



-Conferences — sample counts (dashboard snapshot): 
SEC (116), Big Ten (109), ACC (93), Pac-12 (60), Big 12 (36), Mountain West (23), .... 


-Rookies vs Veterans in dashboard: 
68 rookies and 2,180 veterans → total = 2,248; rookie share = 68 ÷ 2,248 ≈ 0.03025 = 3.03% (so rookies are a small fraction in the dataset shown).



-Top State & regional snapshots:
Top state listed is CA with a metric shown as 545.98 (dashboard label “Top State Fantasy Pts” — interpret carefully: appears to be avg or an aggregate metric shown on dashboard). Top states list: CA, FL, TX, OH, LA. 



-Team-level summary: 
Average Win% ~ 51.20%; total games won ~ 11K; games played ~ 22K. Boise St. appears as a “Top Team” label in the sheet. 

```  




**2) Quick interpretive findings (what these numbers mean)**

```
-Top performers are QB/RB heavy:
The top-10 fantasy list is dominated by QBs (6 of 10) and RBs (4 of 10). That suggests QB production drives high fantasy totals in your period (1999–2013). 



- Combine metrics differ by position:
Average 40/bench/vertical Figures are in the dashboard and vary by position — use boxplots to show overlap (WR/RB speed vs. QB combine profile). 



- College / Conference concentration:
SEC, Big Ten, and ACC produce most players — so college pipeline effects are strong. But top college counts vs fantasy output can differ (one conference may produce many players but lower per-player fantasy yields). 



- Geography matters:
CA / FL / TX dominate counts and fantasy contributions in the dashboard, but you need per-capita normalization (players per 100k residents) to say whether those states are truly overperforming. 



- Rookies are a small share in your snapshot:
With rookies ≈3% of the player rows, most performance in the dataset is driven by veterans. That explains why veteran-driven summary stats dominate. 

```

# ✅ Conclusion

**This Power BI analysis demonstrates that:**

•	Geography matters: States like California, Florida, and Texas dominate NFL talent pipelines.

•	Colleges & Conferences shape the league: The SEC and Big Ten are consistently strong contributors.

•	Player success is multi-factorial: Draft pick, physical attributes, and college pedigree all influence outcomes.

•	Teams thrive on balance: Veteran-heavy teams sustain wins, but rookies provide explosive impact in early years.
The interactive dashboard can be used by analysts, scouts, and fans to explore NFL player pipelines, performance trends, and team strengths in detail.


