# 🎧 Spotify Listening Habits Dashboard

This Power BI dashboard provides an in-depth analysis of Spotify listening behavior, focusing on shuffle play trends, skip patterns, platform usage, and song end reasons. It was created using cleaned and wrangled streaming data, and offers both descriptive insights and behavioral patterns.

![Spotify Dashboard](/images/image.PNG)

## [View Dashboard Here](https://gustavus365-my.sharepoint.com/:u:/g/personal/rboahene_gustavus_edu/ESHimeahxyVPpCrBYdSbfV8BUOBSSZpmPlw8V0pQcoaisg?e=zrte54)

## 📊 Dashboard Overview

### ✅ Key Metrics

- **Total Shuffle Plays:** `112K`
- **Skip Rate:** `5.25%`
- **Total Skips:** `7869`

### 📱 Platform Usage

- **Android** is the dominant platform, with over 100,000 plays.
- Usage on other platforms like iOS, Windows, macOS, and Web Player is comparatively minimal.

### ⏩ Skip Behavior

- **Top skip reasons:**
  - `popup` (highest skip rate)
  - `unknown`
  - `appload`
- These indicate skips due to UX interruptions or app behavior rather than user intent.

### 🔄 Shuffle Play Analysis

- A majority of plays are done **with shuffle enabled**.
- **Shuffle behavior by reason** reveals that:
  - `trackdone` and `fwdbtn` have higher shuffle percentages.
  - Other reasons like `appload`, `clickrow`, and `playbtn` have lower shuffle interaction.

### 🛑 Track End Reasons

- Most tracks end due to **natural completion (`trackdone`)** or **user-forwarding (`fwdbtn`)**.
- A small number end due to `logout`, `unexpected-exit`, or `unknown` reasons.

### 🎯 Event Reason Distribution

- **Start reasons** show:
  - `trackdone` accounts for over 51% of plays.
  - `fwdbtn` and `clickrow` contribute a large chunk of intentional user plays.
- This suggests a healthy mix of passive listening and user-driven behavior.

---

## 🧹 Data Wrangling & Transformation Insights

The raw Spotify listening data was preprocessed using the following techniques:

### ✅ Cleaning

- **Null handling:** Removed or imputed missing values in key columns like `Reason Start`, `Reason End`, and `Platform`.
- **Deduplication:** Filtered duplicate event logs to maintain accuracy of counts.
- **Date/Time parsing:** Timestamp fields were parsed for temporal analysis (e.g., future time series).

### 🔄 Transformation

- **Categorical encoding:** Grouped rare categories (e.g., low-frequency platforms) for clearer visualization.
- **Aggregation:** Metrics like skip rate and shuffle percentage were calculated using grouped aggregations.
- **Derived metrics:**
  - `Skip Rate = Total Skips / Total Plays`
  - `Shuffle % = Shuffle Plays / Total Plays by Reason`

### 🛠 Tools Used

- **Power BI** for dashboard creation and DAX measures.
- **Power Query Editor** for data cleaning and transformations.

---

## 💡 Insights & Takeaways

- **User experience matters:** High skip rates for `popup` and `appload` suggest UX-related interruptions lead to disengagement.
- **Shuffle dominates:** Most listening occurs in shuffle mode, especially for tracks that are auto-played (`trackdone`).
- **Forwarding behavior** is a significant indicator of active engagement, especially via the `fwdbtn` reason.

---

## 📁 Files

| File                                                                                                     | Description                                     |
| -------------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| `spotify_dashboard.pbix`                                                                                 | Power BI file containing the complete dashboard |
| `README.md`                                                                                              | Project documentation                           |
| `[data/spotify_listening](https://www.kaggle.com/datasets/anandshaw2001/top-spotify-songs-in-countries)` | Raw or cleaned Spotify data

---

## 📌 Future Enhancements

- Add **time-series insights** (listening habits over time).
- Incorporate **demographics or user metadata** (if available).
- Track **genre-level engagement** to refine recommendation models.
