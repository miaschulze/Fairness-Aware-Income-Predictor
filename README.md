<h1>Fairness-Aware Income Prediction</h1>

<h2>Description</h2>
This project audits and mitigates gender bias in income prediction models using the UCI Audit Income dataset. It explores fairness issues by analyzing how Logistic Regression models can produce unequal outcomes between male and female groups. Using fairlearn, the code performs bias detection through selection rate and demographic parity metrics, and then applies Exponentiated Gradient mitigation to reduce bias while maintaining predictive performance. Bar plots before and after mitigation clearly visualize fairness improvements across groups.

<h2>Why This Matters</h2>
Machine learning models are increasingly used in high-stakes domains like hiring, lending, insurance, and criminal justice. However, without proper auditing, these models can unintentionally amplify societal biases present in historical data - leading to unfair treatment of individuals based on gender, race, or other sensitive attributes. By identifying and correcting bias in predictive systems, we can build models that are not only accurate, but also equitable. This project demonstrates practical steps any data scientist can take to make ML models more transparent and accountable.

<h2>Languages and Libraries Used</h2>

- <b>Python</b>  
- <b>Pandas</b>  
- <b>NumPy</b>  
- <b>Matplotlib</b>  
- <b>Seaborn</b>
- <b>Scikit-learn</b>
- <b>Fairlearn</b>  

<h2>Environments Used</h2>

- <b>Google Colab</b>  
- <b>Jupyter Notebook</b>  
- <b>Python 3.11+</b>

<h2>Models Implemented</h2>

- <b>Logistic Regression:</b> Trained on preprocessed features to predict whether an individual earns over $50K annually.
- <b>Fairness MetricFrame Analysis:</b> Used to compute group-based selection rates and demographic parity differences for the sensitive attribute sex.
- <b>Exponentiated Gradient Mitigation:</b> Applied to enforce Demographic Parity using Fairlearn, retaining the classifier to reduce bias.
- <b>Accuracy Evaluation:</b> Compared model performance before and after mitigation to evaluate trade-offs between fairness and accuracy.

<h2>Metric Summary</h2>
Before applying mitigation, the model achieved an accuracy of 84.5% but exhibited a significant gender disparity:

- The selection rate for males (predicted income > $50K) was 17%, while for females it was only 5%.
- This resulted in a demographic parity difference of 0.122, indicating substantial bias.
  
After applying Exponentiated Gradient mitigation using Fairlearn:
- The accuracy slightly decreased to 82.1%, showing a small trade-off for improved fairness.
The female selection rate increased to 6.7%, while the male selection rate decreased to 9.3%, bringing the groups closer in treatment.
- The demographic parity difference dropped to 0.035, indicating a meaningful reduction in gender bias.

These results demonstrate that fairness interventions can reduce bias without severly compromising model performance.

<h2>Visualizations</h2>

<p align="center">

<b>Before and After Mitigation - Selection Rate by Gender:</b><br/>
<img src="https://imgur.com/n7e9d4g.png" width="80%" alt="Bias Mitigation Chart"/>
