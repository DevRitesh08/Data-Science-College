# Most Runs in Indian Premier League (IPL) – Career Batting Aggregates (2008–2025)

## 1. Overview
This dataset provides consolidated career batting statistics for Indian Premier League (IPL) players from the inaugural 2008 season through the 2025 season (current update point). Each record represents a player’s cumulative performance across all franchises played for. The dataset is suitable for comparative analysis, exploratory data analysis (EDA), feature engineering, and performance modeling in cricket analytics.

## 2. Scope & Structure
- Coverage: IPL seasons 2008–2025  
- Unit of observation: Player (career aggregate; no season-by-season breakdown)  
- File: `Most runs in Indian Premier League.csv`  
- One row per player; columns are primarily numeric except for identifiers and span markers.

## 3. Column Definitions
| Column | Description |
|--------|-------------|
| Player | Player name; parenthetical abbreviations list franchises represented historically. |
| Span | First and last season active (e.g., 2008-2025). |
| Mat | Matches played. |
| Inns | Innings batted. |
| NO | Not-out innings. |
| Runs | Total runs scored. |
| HS | Highest score; `*` indicates not out. |
| Ave | Batting average = Runs / (Inns − NO). |
| BF | Balls faced. |
| SR | Strike rate = (Runs / BF) * 100. |
| 100 | Centuries (scores ≥100). |
| 50 | Half-centuries (scores 50–99). |
| 0 | Ducks (dismissals for 0). Blank cells likely correspond to zero (verify). |
| 4s | Total fours hit. |
| 6s | Total sixes hit. |

## 4. Data Notes & Quality Considerations
- Blank values in `0` (ducks) appear to denote zero; confirm prior to strict statistical use.  
- `HS` contains a non-numeric asterisk for not-out; retain or parse into numeric plus a binary flag.  
- Franchise sequences (e.g., `DC/DCH/MI/PBKS/SRH`) can be parsed to study player movement.  
- No temporal granularity beyond `Span`; time-series or progression analyses will require augmentation.  
- Strike rate and boundary profiles are sensitive to changing league batting conditions over eras; normalization by era is recommended for longitudinal comparisons.

## 5. Potential Analytical Directions
- Comparative profiling of high-run vs high-strike-rate players.
- Clustering (e.g., average, strike rate, boundary percentage, not-out percentage).
- Boundary dependency vs longevity analysis.
- Projection models: estimating time to next career milestone (e.g., 9000 runs).
- Era impact: group players by debut cohorts to study progression in SR norms.
- Relationship between not-out frequency and strike rate (trade-off evaluation).

## 6. Visualization Suggestions
- Top-N runs leaderboard (horizontal bar chart).
- Strike Rate vs Average with bubble size = Matches.
- Boundary_Pct distribution across player cohorts.
- Balls_Per_Boundary vs NotOut_Pct scatter to distinguish roles.
- Radar charts for selected elite players (Ave, SR, Boundary_Pct, NotOut_Pct, Finisher_Index).

## 7. Update & Maintenance
| Aspect | Recommendation |
|--------|----------------|
| Refresh cadence | End of each IPL season (optionally mid-season checkpoints). |
| Metadata | Add `last_updated: YYYY-MM-DD` in README. |
| Change tracking | Maintain `CHANGELOG.md` with version/date and modifications. |
| Extension path | Introduce season-by-season splits in supplemental file. |

## 8. Licensing & Attribution
If the underlying numerical data is compiled from publicly available cricket statistic sources (e.g., major cricket databases or official IPL match archives), ensure redistribution aligns with their terms of use.  
Suggested attribution format (adjust date as needed):  
“Aggregated IPL batting statistics (2008–2025) compiled from publicly available cricket records (accessed YYYY-MM-DD). Cleaned and structured for analytical use.”

Proposed license (if redistribution rights permit): **CC BY 4.0**.  
If rights are uncertain, consider a more restrictive notice or limit sharing.

## 11. Limitations
- No season-level temporal panel for progression analysis.
- No contextual (phase-based: Powerplay / Middle / Death) segmentation.
- No player metadata (nationality, handedness, age, batting position).
- No pairing with bowling or fielding metrics for all-rounders.
- Strike rate inflation over time not normalized.

## 12. Future Enhancements (Planned / Suggested)
- Season-by-season statistics file.
- Role classification (opener, top-order, middle-order, finisher).
- Era-normalized strike rate indices.
- Additional performance ratios (e.g., 50+ conversion rates).
- Integration with bowling/all-round contributions.
- Nationality and handedness enrichment.

## 13. Disclaimer
This is an unofficial aggregated dataset for analytical and educational purposes. Figures should be verified against official league or governing body publications for commercial, regulatory, or journalistic use.

---

## Short Summary (Optional)
Career-level IPL batting aggregates (2008–2025) including matches, innings, not outs, runs, high score, average, balls faced, strike rate, centuries, fifties, ducks, and boundary counts. Includes guidance for cleaning and derived feature generation to support comparative and modeling workflows.
