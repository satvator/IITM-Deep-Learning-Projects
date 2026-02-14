# NPPE-2: Automatic Disfluency Restoration
**🏆 Ranked 35th out of 128 Teams**

## Project Overview
This project was developed for the **Multi-Modal Speech Processing and Natural Language Generation** challenge. The objective was to "restore" disfluencies (filler words like "अम्", "ओह", "हुंह") into clean Hindi transcripts to make them sound more natural and conversational.

## 🛠️ Technical Approach
Instead of a heavy black-box model, this solution uses an **Intelligent Pattern-Based Modeling** approach to learn the linguistic nuances of where human speakers typically pause or use fillers.

### 1. Data Analysis & Pattern Mining
* **Pattern Recognition:** Analyzed 19,902 words in the training set to identify words that commonly precede or follow specific disfluencies.
* **Frequency Targeting:** Identified a target density of **6.76 disfluencies per 100 words** to match human speech patterns.
* **Positional Distribution:** Discovered that fillers are most frequent at the beginning of sentences (~32.6% position mark).

### 2. Intelligent Restoration Model
* **Probabilistic Placement:** Used a combined scoring system based on:
    * **Position Score:** Higher probability at the start of sentences.
    * **Pattern Score:** Learned word-pair associations from the training data.
    * **Spacing Logic:** Ensures natural gaps (average of 14-15 words) between fillers.
* **Randomized Selection:** Implemented controlled randomness to prevent repetitive or robotic-sounding outputs.

## 📈 Performance
* **Kaggle Ranking:** 35/128 teams.
* **Strategy:** Successfully beat the competition baseline (0.31691) using an "intelligent" placement approach rather than simple random insertion.

## 📂 File Structure
* `Automatic_Disfluency_Restoration.ipynb`: The main notebook containing the pattern analysis and restoration logic.
* `requirements.txt`: Necessary Python libraries for execution.
