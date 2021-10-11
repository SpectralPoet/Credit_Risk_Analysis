# Credit_Risk_Analysis
assessment of mock credit default data to test machine learning prediction accuracy for BalancedRandomForestClassifier model vs EasyEnsembleClassifier model



## Overview of the analysis: Explain the purpose of this analysis.

### Results
#### Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all six machine learning models. Use screenshots of your outputs to support your results.

For the purposes of this analysis, the algorithm's scored on high-risk loans are what's important, whereas its scores on low-risk loans are excellent, which is to be expected. When discussing each model, the precision and recall discussed will be those of the high-risk loans, although statistics on its performace for low-risk loans will also be visible via the accompanying screenshot.

![NaiveRandomOversamplingConfusionMatrix](https://user-images.githubusercontent.com/21095468/136713944-6e35f39e-a12f-47a1-9a8d-c5a806bb574f.jpeg)

Naive Random Oversampling:
  balanced accuracy - 0.6461830861645939
  precision - 0.01
  recall - 0.63

![SMOTEOversamplingConfusionMatrix](https://user-images.githubusercontent.com/21095468/136714069-3d4584c5-9630-47ae-ac44-f66117aeea13.jpg)

SMOTE Oversampling:
  balanced accuracy - 0.6288832888147584
  precision - 0.01
  recall - 0.60
  
![UndersamplingConfusionMatrix](https://user-images.githubusercontent.com/21095468/136714238-c32d8f95-15ea-4500-b5bb-281fa34d51b8.jpg)

Undersampling:
  balanced accuracy - 0.6363628122847094
  precision - 0.01
  recall - 0.61
  
![CombinationOverUnderSampling](https://user-images.githubusercontent.com/21095468/136715101-1cbfee43-cd35-467f-9343-f4a0e4b04572.jpg)

Combination Under Over Sampling:
  balanced accuracy - 0.6466887043684607
  precision - 0.01
  recall - 0.69
  
![BalancedRandomForestClassifierMatrix](https://user-images.githubusercontent.com/21095468/136715195-28b47cf9-d528-4bef-a872-cb4e1d1cf061.jpg)

Balanced Random Forest Classifier:
  balanced accuracy - 0.9949142691078174
  precision - 0.55
  recall - 0.59
  
![AdaBoostClassifierConfusionMatrix](https://user-images.githubusercontent.com/21095468/136715205-2da7a693-8ea2-4c74-ba54-ba7588f124c8.jpg)

Ada Boost Classifier:
  balanced accuracy - 0.9428073234524847
  precision - 0.07
  recall - 0.90

### Summary
#### Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. If you do not recommend any of the models, justify your reasoning.

It's worth beginning this analysis summary by saying that recall (how many of the high-risk loans were correctly identified) is essentially the target metric. Except in cases of extremely diminished overall accuracy, not-issuing high risk loans is the fundamental goal. By this metric, with a 90% recall metric, and a 94% balanced accuracy, it's safe to say that the Ada Boost Classifier algorithm is performing extremely well. All other algorithms achieve about 60% recall on the target metric. Unfortunately it is not possible to recommend the Ada Boost Classifier for use, as I do not know what the company's current rate of accurately dropping high-risk loans is. If the company's current methods exceed 90% recall, which is quite possible, then I cannot recommend a model which would lower that accuracy. What I can say is that of those models presented, Ada Boost Classification is the clear choice.
