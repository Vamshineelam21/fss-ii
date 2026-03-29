# Fuzzy Cognitive Maps Tutorial

## Deliverable
03_MentalHealthProductivity_FCM.ipynb — FCM-based Mental Health and Productivity Analysis  
Domain: Student Mental Health & Productivity  
Dataset: Student Mental Health Dataset (multiple features related to psychological and behavioral factors)  
Approach: Scenario Simulation + Intervention (Based on Class Importance - Option B)

---

## Problem Statement

Student productivity is highly influenced by mental health conditions such as stress, anxiety, depression, sleep quality, and social interaction. Understanding how these factors interact is essential for improving academic performance and well-being.

This project uses a Fuzzy Cognitive Map (FCM) to model the causal relationships between mental health factors and productivity. Unlike traditional machine learning models, FCM provides interpretable and causal insights, allowing us to analyze how changes in one factor affect the entire system.

For example, we can directly study how improving sleep or reducing stress impacts productivity and mental well-being.

---

## FCM Design

### Concepts (Nodes):

| Concept        | Description                     | Role                |
|---------------|--------------------------------|---------------------|
| Sleep         | Sleep quality                  | Positive driver     |
| Stress        | Stress level                   | Negative driver     |
| Study         | Study effort                   | Positive driver     |
| Social        | Social interaction             | Supportive factor   |
| Anxiety       | Anxiety level                  | Negative driver     |
| Depression    | Depression level               | Negative driver     |
| Productivity  | Overall performance (target)   | Output concept      |

---

### Causal Edges:

Sleep         → (+0.7) → Productivity  
Stress        → (-0.8) → Productivity  
Study         → (+0.6) → Productivity  
Social        → (+0.4) → Productivity  
Anxiety       → (-0.6) → Productivity  
Depression    → (-0.7) → Productivity  
Stress        → (+0.6) → Anxiety  
Anxiety       → (+0.6) → Depression  
Social        → (-0.5) → Stress  

---

## Notebook Structure

- Imports — fcmpy, numpy, pandas, matplotlib  
- Load Dataset — clean and normalize features to [0,1]  
- Concept Definition — define FCM nodes  
- Weight Matrix — establish causal relationships  
- FCM Graph Visualization — visualize relationships using a network graph  
- Scenario Simulation — simulate different student conditions  
- Healthy Scenario — low stress, high sleep → expected high productivity  
- Stress Scenario — high stress, low sleep → expected low productivity  
- Intervention Scenario — improved sleep and reduced stress  
- Results Visualization — compare all scenarios using plots  
- Key Findings — interpret results  
- Conclusion — summarize insights and recommendations  

---

## Key Findings

- A healthy student (high sleep, low stress, low anxiety) converges to significantly higher productivity levels compared to a stressed student.  
- A stressed student (high stress, anxiety, and depression) shows a sharp decline in productivity, highlighting the strong negative influence of mental health factors.  
- The intervention scenario (improving sleep and reducing stress) leads to a noticeable increase in productivity, demonstrating the effectiveness of combined improvements.  
- Stress, anxiety, and depression are the strongest negative drivers of productivity, while sleep and study effort are the most influential positive factors.  
- Social interaction contributes indirectly by reducing stress and improving emotional stability.  

---

## Conclusion

This project demonstrates how Fuzzy Cognitive Maps can effectively model complex relationships between mental health and productivity. The simulation results show that productivity is not influenced by a single factor but by the interaction of multiple variables.

The findings suggest that improving sleep quality, reducing stress, and encouraging social interaction can significantly enhance student productivity. A combined intervention approach yields better results than focusing on individual factors.

Overall, FCM provides a powerful and interpretable framework for analyzing real-world systems and supporting decision-making in areas such as mental health and performance.
