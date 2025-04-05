# Foundation Questions for Machine Learning

## Table of Contents

- [Introduction](#introduction)
- [Key Categories of Foundation Questions](#key-categories-of-foundation-questions)
  - [Problem Definition](#problem-definition)
  - [Data and Assumptions](#data-and-assumptions)
  - [Performance and Ethics](#performance-and-ethics)
  - [Maintenance Planning](#maintenance-planning)
- [Connection to Cognitive Prompt Architecture (CPA)](#connection-to-cognitive-prompt-architecture-cpa)
- [Practical Examples](#practical-examples)
- [Comprehensive Analysis](#comprehensive-analysis)
  - [Detailed Question Framework](#detailed-question-framework)
- [Quick Reference Checklist](#quick-reference-checklist)
- [References](#references)

## Introduction

Foundation questions are essential for establishing a clear understanding before starting a machine learning project. They help identify the problem, assess data availability, and make informed assumptions, ensuring the project is well-planned and effective.

## Key Categories of Foundation Questions

### Problem Definition

Start by asking: What is the specific problem we are trying to solve? Is it classification, regression, or clustering? This clarifies the goal and sets the direction for the project.

### Data and Assumptions

Next, consider the data: What do we have, and are there labeled or unlabeled examples? What assumptions, like data distribution, are we making? These questions ensure the data fits the problem and the model can learn from it.

### Performance and Ethics

How will we measure success, using metrics like accuracy or F1-score? Also, are there ethical risks, like bias, that need addressing? This ensures the model is fair and meets project goals.

### Maintenance Planning

An often overlooked aspect is asking how the model will be maintained and updated over time, especially if data changes, ensuring long-term relevance and effectiveness.

## Connection to Cognitive Prompt Architecture (CPA)

The Foundation Questions framework serves as an essential precursor to applying the Cognitive Prompt Architecture (CPA). By thoroughly addressing these questions, you establish the groundwork needed to effectively utilize CPA's domains:

- **Problem Definition** → Prepares you for the **Reasoning Cycle (RC)** domain by clarifying what solution approaches to explore
- **Data and Assumptions** → Enables effective use of the **Dialectic Inquiry (DI)** domain by identifying assumptions to question
- **Performance and Ethics** → Supports the **Adversarial Refinement (AR)** domain by establishing criteria to challenge solutions against
- **Maintenance Planning** → Aligns with the **Evolutionary Growth (EG)** domain's focus on iterative improvement

Answering these foundation questions creates the context within which CPA can operate most effectively, ensuring your cognitive prompts are grounded in a clear understanding of the problem space.

## Practical Examples

Let's explore how foundation questions apply to real machine learning projects:

### Example 1: Customer Churn Prediction

**Problem Definition:**
- *Question:* What is the specific problem we are trying to solve?
- *Answer:* We need to predict which customers are likely to cancel their subscription in the next 30 days (a binary classification problem).

**Data and Assumptions:**
- *Question:* What data do we have available?
- *Answer:* We have 18 months of customer behavior data including usage patterns, billing history, and support interactions. We have 50,000 labeled examples with 15% churn rate.
- *Question:* What assumptions are we making?
- *Answer:* We assume that past behavior patterns leading to churn will continue to be relevant in the future, and that our 15% churn rate in historical data is representative of the current customer base.

**Performance and Ethics:**
- *Question:* How will we measure success?
- *Answer:* We'll prioritize recall over precision (F2-score) since the cost of missing a churning customer is higher than the cost of offering retention incentives to non-churning customers.
- *Question:* Are there ethical considerations?
- *Answer:* We need to ensure our model doesn't discriminate based on demographic factors and that retention offers are fair across customer segments.

**Maintenance Planning:**
- *Question:* How will the model be updated?
- *Answer:* We'll retrain monthly with new data and conduct a full model review quarterly to check for concept drift, especially after product or pricing changes.

### Example 2: Medical Image Classification

**Problem Definition:**
- *Question:* What is the specific problem we are trying to solve?
- *Answer:* We need to classify chest X-rays into normal or abnormal, with abnormal further categorized into 5 specific conditions (a multi-class classification problem).

**Data and Assumptions:**
- *Question:* What data do we have available?
- *Answer:* We have 10,000 labeled X-ray images from three different hospitals, with annotations from radiologists. The dataset has class imbalance with some conditions having fewer than 500 examples.
- *Question:* What assumptions are we making?
- *Answer:* We assume that the image quality and annotation standards are consistent across hospitals, and that the conditions present in our training data cover the spectrum of conditions we'll encounter in deployment.

**Performance and Ethics:**
- *Question:* How will we measure success?
- *Answer:* We'll use class-weighted F1-scores and confusion matrices to ensure performance across all conditions. We require >90% sensitivity for critical conditions.
- *Question:* Are there ethical considerations?
- *Answer:* The model must perform consistently across demographic groups. We need transparency in decision-making for medical professionals to understand and verify model outputs.

**Maintenance Planning:**
- *Question:* How will the model be updated?
- *Answer:* We'll implement a human-in-the-loop system where radiologists can flag incorrect predictions, creating a feedback loop for continuous improvement. Quarterly model updates will incorporate new validated data.

## Comprehensive Analysis

This section provides a detailed exploration of foundational questions in machine learning, focusing on establishing a deep understanding through targeted inquiries about problems and assumptions. The analysis is grounded in a review of various resources, including books, articles, and online platforms, to ensure a thorough and professional presentation.

### Introduction to Foundation Questions

Foundation questions in machine learning are critical for setting the stage for successful projects. They involve a systematic approach to understanding the problem, data, and assumptions, ensuring that all aspects are considered before model development begins. These questions are not standardized under a single term like "Foundation Questions," but they align with best practices for initiating machine learning initiatives, as discussed in industry blogs and textbooks.

The process of asking these questions helps in clarifying objectives, assessing data readiness, and identifying potential challenges, such as ethical implications or computational constraints. This survey note compiles a comprehensive list of such questions, supported by examples and references, to provide a robust framework for practitioners.

### Detailed Question Framework

| **Category**               | **Specific Questions**                                                                 | **Purpose**                                                                 |
|----------------------------|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| Problem Definition         | What is the specific problem we are trying to solve? Is it classification, regression, or clustering? | Clarifies the goal and sets the project direction.                          |
| Data Understanding         | What data do we have available? Are there labeled or unlabeled examples? What is the size of the dataset? Are there missing values or outliers? | Ensures data suitability and identifies preprocessing needs.                |
| Assumptions                | What assumptions are we making about the data distribution (e.g., normal distribution)? Are there assumptions about feature-target relationships? | Validates model assumptions and ensures alignment with data characteristics.|
| Performance Metrics        | How will we measure success? What metrics like accuracy, precision, recall, F1-score, or R-squared are appropriate? | Defines success criteria and evaluation methods.                            |
| Model Selection            | What type of model is best suited for this problem? What are the strengths and weaknesses of potential models? | Guides the choice of algorithms based on problem and data.                  |
| Validation Strategy        | How will we validate the model to ensure generalization? What is the train-test split or cross-validation strategy? | Ensures the model performs well on unseen data.                             |
| Interpretability           | Is it important to understand why the model makes certain predictions? Do we need an interpretable model? | Addresses needs for transparency, especially in critical applications.      |
| Scalability                | Does the model need to handle large datasets efficiently? What computational resources are available? | Ensures feasibility given resource constraints.                             |
| Ethical Considerations     | Are there ethical implications of the model's predictions? Is there a risk of bias in the data or model? | Mitigates risks of unfair outcomes and ensures ethical compliance.          |
| Maintenance and Updating   | How will the model be maintained and updated over time? Is the data stationary, or does it change, requiring retraining? | Ensures long-term relevance and adaptability to changing data.              |

This table encapsulates the essential inquiries, drawn from resources like Skim AI's checklist for starting machine learning projects, which provides practical guidance on data and problem assessment.

#### Supporting Resources and Context

The compilation of these questions is informed by several key sources. For instance, "Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow" by Aurélien Géron (2019) discusses the importance of problem definition and data understanding in its initial chapters, emphasizing the need for clear objectives and data readiness. Similarly, "Machine Learning: A Probabilistic Perspective" by Kevin Murphy (2012) provides a theoretical foundation for understanding assumptions, such as data distribution, which is crucial for model selection.

Online resources, such as Skim AI's article "10 Questions to Ask Before Starting a Machine Learning Project" ([10 Questions to Ask Before Starting a Machine Learning Project](https://skimai.com/checklist-starting-a-machine-learning-project/)), offer practical insights, including specific numbers like needing 2,000–5,000 data points per category for effective labeling, and considerations for metadata availability. These details enhance the practical applicability of the questions listed.

An unexpected detail from the analysis is the emphasis on maintenance and updating, often overlooked in initial planning. This aspect, highlighted in discussions on long-term model relevance, ensures that models remain effective as data evolves, a critical consideration for real-world applications.

#### Application and Implications

These foundational questions are not only theoretical but also have practical implications. For example, asking about ethical considerations can prevent biased outcomes, a growing concern in machine learning applications, as noted in discussions on AI ethics. The questions also facilitate collaboration between data scientists and stakeholders, ensuring alignment on goals and expectations.

The analysis also reveals that while some questions, like data size and labeling, have specific benchmarks (e.g., 5,000 data points minimum for human accuracy), others, like ethical risks, require qualitative assessment and may vary by context. This flexibility is essential for adapting the framework to different industries and project scopes.

#### Conclusion

In conclusion, establishing a foundational understanding through targeted questions about the problem and assumptions is a cornerstone of successful machine learning projects. The detailed list provided, supported by authoritative sources, offers a comprehensive guide for practitioners. It ensures that all critical aspects, from data readiness to ethical considerations, are addressed, paving the way for robust and effective machine learning solutions.

## Quick Reference Checklist

Use this checklist before starting any machine learning project to ensure you've covered all essential foundation questions:

### Problem Definition
- [ ] Clearly defined the specific problem to solve
- [ ] Identified the type of ML task (classification, regression, clustering, etc.)
- [ ] Established clear success criteria for the project
- [ ] Determined if ML is actually the right approach for this problem

### Data and Assumptions
- [ ] Inventoried all available data sources and their characteristics
- [ ] Assessed data quantity (sufficient examples for each class/outcome)
- [ ] Evaluated data quality (missing values, outliers, noise)
- [ ] Documented assumptions about data distribution and relationships
- [ ] Identified potential biases in the data collection process

### Performance and Ethics
- [ ] Selected appropriate evaluation metrics aligned with business goals
- [ ] Established minimum performance thresholds for deployment
- [ ] Identified potential ethical risks and mitigation strategies
- [ ] Considered fairness across different user groups or demographics
- [ ] Planned for model interpretability and explainability needs

### Maintenance Planning
- [ ] Developed strategy for monitoring model performance in production
- [ ] Created plan for handling concept drift and data distribution changes
- [ ] Established retraining frequency and triggers
- [ ] Defined roles and responsibilities for model maintenance
- [ ] Documented procedures for model updates and versioning

## References

-   Géron, A. (2019). Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow: Concepts, Tools, and Techniques to Build Intelligent Systems (2nd ed.). O'Reilly Media. [Link](https://www.oreilly.com/library/view/hands-on-machine-learning/9781492032632/)
-   Murphy, K. P. (2012). Machine Learning: A Probabilistic Perspective. MIT Press. [Link](https://mitpress.mit.edu/9780262018029/machine-learning/)
-   Skim AI. (2023). 10 Questions to Ask Before Starting a Machine Learning Project. [Link](https://skimai.com/checklist-starting-a-machine-learning-project/)
-   Amershi, S., Begel, A., Bird, C., DeLine, R., Gall, H., Kamar, E., Nagappan, N., Nushi, B., & Zimmermann, T. (2019). Software Engineering for Machine Learning: A Case Study. In 2019 IEEE/ACM 41st International Conference on Software Engineering: Software Engineering in Practice (ICSE-SEIP) (pp. 291-300). IEEE.
