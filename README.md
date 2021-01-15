# MushroomClassification

Foraging for wild mushrooms is a deadly endeavor
Telling poisonous mushrooms apart from edible ones is difficult, even for experienced harvesters. 1500 people are hospitalized in the US every year with possible permanent damage, with 5-10 deaths. It would be beneficial to develop a system to help amateurs forage for mushrooms safely.

The dataset came from amateur scientists
The Audobon Society produced the dataset. It contains 8124 instances and 23 columns of categorical variables. One column contained missing values and was dropped.

Two different models were used

Before modeling, the data was prepared by one-hot encoding all independent variables. The data was split into 80% training 20% testing datasets. The end shapes of these datasets were (6498, 112) and (1625, 112).

Both a tree model and a KNeighbors model were fitted to this data, as neither provided a unique benefit to this dataset. 

Both models seem too accurate 

Accuracy metrics and confusion matrices were applied. to the models Both models had the same result: 

Train Accuracy: 1.0
Test Accuracy: 1.0
[[831, 0]
[0, 794]]

This suggests too many factors were used in evaluation, as a 100% success rate is highly unusual and almost suspiciously accurate.

The ANOVA results showed the most important factors
It is difficult to pick out important variables from a list of 112. Based on the ANOVA table, the most important factors in poison detection are:
Odor (none): F=5.3376, P=.0672
Spore Print Color (Green):
F=4.8013, P=.0285

Mushrooms are predictable
Toxicity can be predicted in mushrooms. In the families Agaricus and Lepiota, the most important are odor and the color of the spore print. No odor indicates an edible mushroom, while a green spore print indicates poison. 

Dataset Used
https://archive.ics.uci.edu/ml/datasets/Mushroom
Mushroom fatality statistics: https://eattheplanet.org/foraging-fatality-statistics-2016/
