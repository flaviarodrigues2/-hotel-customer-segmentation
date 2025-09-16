# Hotel Customer Segmentation (Business Case Project)

Academic project for the **Business Cases with Data Science** course, part of the Master’s in **Data Science and Advanced Analytics**.  
The goal was to build a **customer segmentation model** for a hotel in Lisbon, leveraging clustering techniques to enable more effective marketing strategies and improve customer retention.

## Objectives
- Understand customer profiles using **demographic, geographic, behavioral and preferential data**.  
- Apply **K-Means clustering** to identify distinct customer segments.  
- Use **Principal Component Analysis (PCA)** to reduce dimensionality and improve model interpretability.  
- Translate analytical findings into **business applications** to support tailored marketing initiatives.  

## Dataset
- **111,733 customer profiles**  
- Variables include: nationality, age, lead time, revenues (lodging & other), booking behaviors (cancellations, no-shows, check-ins), stay metrics (PersonNights, RoomNights), distribution channels, and room preferences (e.g., quiet room, crib, king-size bed).  

## Data Preparation
- Removed duplicates and consolidated multiple profiles per customer.  
- Cleaned invalid data (negative ages, inconsistent IDs, incorrect revenue records).  
- Missing values imputed with **KNN**.  
- Feature engineering:  
  - `TimeBetweenVisits`, `CheckInRatio`, continent instead of nationality.  
- Feature transformation: binning of continuous variables, one-hot encoding for categorical features, MinMax scaling.  
- Dimensionality reduction with **PCA** to retain most relevant variance.  

## Modeling
- **K-Means clustering** applied with the **elbow method** and silhouette scores to select the optimal K.  
- Segmentation strategy combined:  
  - **A priori** segmentation (loyalty program users vs hotel stayers).  
  - **Post hoc** segmentation via K-Means on the remaining customers.  
- Final model identified **six main clusters**, each with distinct behaviors, demographics and spending patterns.  

## Results – Cluster Profiles
- **Cluster 0: Youth Adventurers** – younger guests, budget-conscious, prefer travel agents.  
- **Cluster 1: Diverse High Spenders** – cross-age group, high revenue, direct bookings, family-oriented.  
- **Cluster 2: Senior Globetrotters** – older customers, international, cultural/leisure focus.  
- **Cluster 3: Mature Leisure Enthusiasts** – experienced travelers, high spend on hotel facilities, advance planners.  
- **Cluster 4: Midlife Explorers** – 40–55, corporate bookings, Oceania presence.  
- **Cluster 5: Last-Minute Visitors** – spontaneous European travelers, low revenue, agency bookings.  

## Business Applications
- Tailored marketing campaigns for each cluster (youth packages, exclusive experiences, senior partnerships, leisure-focused offers, corporate retreats, last-minute deals).  
- Channel strategies: social media (Instagram, TikTok), travel agencies, LinkedIn, email marketing.  
- Revenue growth through targeted promotions, loyalty programs, and B2B partnerships.  

## Team
Group R – Business Cases with Data Science 2023/24
