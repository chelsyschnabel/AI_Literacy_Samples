# AI Literacy: Undergraduate Computer Science

## Overview

This is a semester-long independent study for undergraduate research, focusing on machine learning.

**Subject:** Computer Science - Machine Learning Applications  
**Suggested Tools:** GitHub Copilot, ChatGPT-4, Claude, Academic databases  
**Duration:** Full semester independent study  
**Learning Objective:** Using AI to accelerate development while maintaining research rigor and originality

## Research Project: "Bias Detection in Natural Language Processing Models: A Comparative Analysis of Mitigation Strategies"

### Project Overview:
Independent research examining gender and racial bias in sentiment analysis models, comparing effectiveness of different bias mitigation techniques.

### Phase 1: Literature Review and Hypothesis Development (Weeks 1-3)

*Research Questions:*
1. How do different pre-processing techniques affect bias in sentiment analysis models?
2. Which post-processing bias mitigation strategies are most effective across different demographic groups?
3. How do these strategies affect overall model performance?

*AI-Enhanced Literature Strategy:*
*Student approach:* Used AI to help navigate the rapidly evolving ML bias literature
*Sample interaction:*
"I'm researching bias in NLP models. The literature is vast and changes quickly. Can you help me identify the most influential recent papers on bias mitigation techniques and suggest how to organize my literature review to cover the key approaches systematically?"

*Literature Review Results:*
- Identified 45 relevant papers using AI-suggested search strategies
- Used ChatGPT to help understand complex mathematical formulations in bias metrics
- Created systematic comparison of bias detection methods with AI assistance in organizing frameworks

### Phase 2: Experimental Design (Weeks 4-5)

*Dataset Selection Process:*
*Student decision-making with AI input:*
"I need to choose datasets for testing bias in sentiment analysis. I'm considering IMDb reviews, Twitter sentiment, and product reviews. Can you help me think through the advantages and limitations of each for studying demographic bias?"

*Final Experimental Design:*
- Three datasets: IMDb movie reviews, Twitter sentiment140, Amazon product reviews
- Four bias mitigation techniques: data augmentation, adversarial debiasing, post-processing calibration, and ensemble methods
- Evaluation metrics: accuracy, demographic parity, equalized odds, individual fairness

### Phase 3: Implementation and Development (Weeks 6-10)

*Code Development with AI Assistance:*
*Student's approach:* Used GitHub Copilot for coding efficiency while maintaining understanding of all implementations

*Example AI-Assisted Implementation:*
```python
class BiasMetrics:
    """
    Custom implementation of bias detection metrics for sentiment analysis
    Student wrote core logic, used Copilot for optimization suggestions
    """
    
    def __init__(self, protected_attributes):
        self.protected_attributes = protected_attributes
        # Student designed architecture, AI suggested improvements
    
    def demographic_parity(self, y_pred, sensitive_attr):
        """
        Calculate demographic parity across groups
        Mathematical formulation developed by student
        Implementation optimized with AI suggestions
        """
        groups = np.unique(sensitive_attr)
        positive_rates = {}
        
        for group in groups:
            group_mask = sensitive_attr == group
            group_predictions = y_pred[group_mask]
            positive_rates[group] = np.mean(group_predictions)
        
        # AI suggested using statistical tests for significance
        return self._calculate_parity_difference(positive_rates)
    
    def equalized_odds(self, y_true, y_pred, sensitive_attr):
        """
        Student-designed implementation with AI optimization
        """
        # Implementation details...
        pass
```

*AI Interaction Documentation:*
*Student's research log entry:*
"Used GitHub Copilot extensively for implementing standard ML operations (data loading, model training loops) but wrote all bias metric calculations myself to ensure I understood the mathematics. When Copilot suggested optimizations, I evaluated each suggestion and only incorporated those I could explain and justify."

### Phase 4: Experimental Results and Analysis (Weeks 11-13)

*Experimental Findings:*
- Data augmentation most effective for gender bias (23% reduction in bias metrics)
- Adversarial debiasing showed best results for racial bias (31% reduction)
- Post-processing methods maintained highest overall accuracy
- Ensemble approaches provided most balanced performance across metrics

*AI-Assisted Analysis:*
*Statistical Significance Testing:*
*Student prompt:* "I have experimental results comparing four bias mitigation techniques across three datasets. My results show different techniques work best for different types of bias. Can you help me design appropriate statistical tests to determine if these differences are significant and suggest how to present these results clearly?"

*Advanced Analysis with AI Support:*
- Implemented bootstrap confidence intervals for bias metrics
- Used AI to help interpret interaction effects between mitigation strategies
- Developed visualization strategies for multi-dimensional results

### Phase 5: Implications and Future Work (Weeks 14-15)

*Novel Contributions:*
1. First systematic comparison of these specific techniques across these datasets
2. Development of ensemble approach combining best aspects of different methods
3. Analysis of trade-offs between bias reduction and model performance

### Final Research Paper Excerpts:

**Abstract:**
"This study presents a comprehensive evaluation of bias mitigation strategies for sentiment analysis models across gender and racial demographics. Through systematic experimentation on three diverse datasets, we demonstrate that optimal bias mitigation strategies vary by bias type and application context. Our novel ensemble approach achieves a 28% average reduction in bias metrics while maintaining 94% of original model accuracy."

**Methodology - AI Use Statement:**
"This research employed AI tools strategically to enhance productivity while maintaining research integrity. GitHub Copilot assisted with standard coding tasks, allowing focus on novel algorithmic development. ChatGPT helped interpret complex mathematical formulations in the literature and suggested statistical analysis approaches. All experimental design, hypothesis formation, and result interpretation remained entirely under researcher control. Complete documentation of AI interactions is provided in the supplementary materials."

**Discussion:**
"These findings challenge the assumption that a single bias mitigation approach will be universally effective. The variation in optimal strategies across demographic groups and datasets suggests that practical bias mitigation systems should employ adaptive approaches that can select appropriate techniques based on the specific context and bias types present."

**Future Work:**
"Building on these findings, future research should investigate dynamic bias mitigation systems that can automatically select optimal strategies based on detected bias patterns. Additionally, the trade-offs identified between bias reduction and model performance warrant investigation into techniques that can achieve better optimization of both objectives simultaneously."

**Research Impact:**
- Paper accepted at undergraduate research conference
- Code and datasets made publicly available on GitHub
- Methods adopted by two local tech companies for their bias testing protocols