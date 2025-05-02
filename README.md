# 🐦 Twitter Friends Analysis

This project explores and analyzes a dataset of 40,000 Twitter users, focusing on their social connections, including followers and friends. The goal is to understand patterns in user engagement, behavior, and connectivity on the Twitter platform using exploratory data analysis and interactive visualizations.

---

## 📊 Dataset Overview

The dataset contains records for **40,000 Twitter users**, each with details such as:

- `id`: Unique user ID  
- `screenName`: Twitter handle  
- `tags`: Hashtags used in their tweets  
- `avatar`: Profile image URL  
- `followersCount`: Number of followers  
- `friendsCount`: Number of friends (accounts the user follows)  
- `lang`: Language of the user's tweets (all are "en")  
- `lastSeen`: Timestamp of the user's last activity  
- `tweetId`: ID of the user's most recent tweet  
- `friends`: List of friend IDs (connections)  

---

## 🧹 Data Preprocessing

- 🧼 Quotes were stripped from string and numerical fields for proper parsing.  
- 🔍 JSON strings in `tags` and `friends` columns were parsed into Python objects.  
- 🗑️ Dropped unnecessary columns: `lang`, `avatar`, and `tweetId` due to low analytical value.  
- 📅 Converted `lastSeen` from timestamp to human-readable date format.  

---

## 📈 Exploratory Data Analysis

### Followers Distribution

- 📉 Most users have **fewer than 1,000 followers**.
- 📊 Very few users exceed **100,000 followers**.
- A clear **long-tail distribution** is observed in follower counts.

### Friends (Following) Distribution

- 📉 Similar to followers, most users follow **a modest number of accounts**.
- Some users follow **tens of thousands of other users**, potentially bots or marketers.

### Followers vs Friends

- 🔁 Scatter plots show a **positive correlation** between followers and friends, though with high variability.
- 🕵️ Some users follow many but have few followers (possibly inactive or spam accounts).

### Activity Timeline

- ⏳ Most `lastSeen` dates are concentrated between **August 26–27, 2016**, with very few on later dates.
- 📅 Converted timestamps into readable dates for better visualization.

---

## 📊 Visualizations

- 📦 Histograms: Distribution of `followersCount` and `friendsCount`.
- 📍 Logarithmic scatter plots: Followers/Friends grouped by exponential ranges.
- 📅 Time series: User activity vs followers and friends across `lastSeenDatetime`.
- 🖱️ Interactive plots with hover details using Plotly.

---

## 💡 Insights & Observations

- 🤝 The dataset reflects **high social activity** in a narrow time window, possibly due to a specific event or scraping batch.
- 🧠 Most Twitter users are **moderately connected**; extreme outliers may indicate influential users or bots.
- 📊 Data is rich for further **network analysis**, e.g., identifying influencer nodes or community clusters.

---

## 🚀 Future Work

- 🌐 Build **graph-based network analysis** using `friends` relationships.
- 🧠 Apply **clustering or centrality algorithms** to detect influencers or communities.
- 🔍 Sentiment or hashtag analysis from `tags` to understand topics driving engagement.
- 📈 Incorporate **temporal activity trends** to study user churn or retention.

---

## 🛠️ Technologies Used

- 🐍 Python (Pandas, NumPy)
- 📊 Plotly (for interactive visualizations)
- 📘 Jupyter Notebook

