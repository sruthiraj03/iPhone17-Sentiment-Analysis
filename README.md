# Reddit Sentiment Analysis of iPhone 17

## Overview
This project analyzes Reddit discussions surrounding the iPhone 17 to understand public sentiment, key discussion themes, and user engagement following the product launch. Using natural language processing techniques, the analysis connects sentiment and topic trends to actionable business insights.

## Business Motivation
Consumer perception plays a critical role in the success of major product launches. Reddit provides long-form, community-driven discussions that surface honest opinions, frustrations, and praise. Understanding these conversations helps identify:
- Which features resonate most with users
- Which issues create negative sentiment
- How engagement varies across themes and sentiment

## Data Collection
- **Source:** Reddit
- **Method:** PRAW API (Python)
- **Volume:** ~2,600 posts
- **Subreddits:** iPhone17, iPhone17Pro, iPhone, iPhoneography, iOSsetups, patinaproud, ATT
- **Filtering:** English-only posts published after the iPhone 17 announcement

Duplicate posts and empty text entries were removed prior to analysis.

## Methodology

### Sentiment Analysis
- Applied **VADER** sentiment scoring to each post
- Classified posts as **Positive**, **Negative**, or **Neutral** using standard thresholds
- Added sentiment scores and labels for downstream analysis

### Topic Modeling
- Split data into positive and negative sentiment subsets
- Applied **LDA (Latent Dirichlet Allocation)** with CountVectorizer
- Extracted five core topics per sentiment category
- Interpreted topics using top contributing words

### Engagement Metric
Created a custom engagement metric combining:
- Post frequency
- Normalized Reddit score (upvotes)

This captures both how often topics are discussed and how strongly users interact with them.

## Key Findings

### Sentiment Distribution
- Positive sentiment dominated discussions
- Negative sentiment represented a smaller but meaningful share
- Neutral posts generated moderate engagement

### High-Engagement Topics
**Positive Themes**
1. Aesthetic & Display
2. Camera Quality & Battery Performance
3. Upgrade Value & Purchase Experience

**Negative Themes**
1. General Device Complaints
2. Trade-In & Ordering Experience (notably AT&T)
3. Battery Performance Issues

Battery performance and purchase experience appeared in both positive and negative sentiment, indicating mixed but largely favorable perception.

## Business Insights
- Design choices (aesthetics, display, camera) are strong drivers of positive engagement
- Durability concerns pose reputational risk
- Friction in third-party retail experiences contributes significantly to negative sentiment
- Marketing should emphasize design and camera upgrades, while operational improvements should address durability and retail coordination

## Tools & Libraries
- Python
- PRAW (Reddit API)
- NLTK (VADER)
- scikit-learn
- pandas, numpy

## Contributors
Andrea Pan · Angie Pang · Carson Pimental · **Jaya Sruthi Raj Perikala**
