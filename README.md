# Dry-Beans-Classification-Competition

This is For [InClass Prediction Competition](https://www.kaggle.com/competitions/dry-beans-classification-iti-ai-pro-intake01)

---

## description 
- the goal was to predict predict the type of each bean out of 7 bean types in this dataset.
- You are provided a set of features extracted from the shape of the beans in images
- ---


## File descriptions
- train.csv - the training set.
- test.csv - the test set.
- sample_submission.csv - a sample submission file in the correct format

---

## Data fields
* ID - an ID for this instance
* Area - (A), The area of a bean zone and the number of pixels within its boundaries.
* Perimeter - (P), Bean circumference is defined as the length of its border.
* MajorAxisLength - (L), The distance between the ends of the longest line that can be drawn from a bean.
* MinorAxisLength - (l), The longest line that can be drawn from the bean while standing perpendicular to the main axis.
* AspectRatio - (K), Defines the relationship between L and l.
* Eccentricity - (Ec), Eccentricity of the ellipse having the same moments as the region.
* ConvexArea - (C), Number of pixels in the smallest convex polygon that can contain the area of a bean seed.
* EquivDiameter - (Ed), The diameter of a circle having the same area as a bean seed area.
* Extent - (Ex), The ratio of the pixels in the bounding box to the bean area.
* Solidity - (S), Also known as convexity. The ratio of the pixels in the convex shell to those found in beans.
* Roundness - (R), Calculated with the following formula: (4piA)/(P^2)
* Compactness - (CO), Measures the roundness of an object: Ed/L
* ShapeFactor1 - (SF1)
* ShapeFactor2 - (SF2)
* ShapeFactor3 - (SF3)
* ShapeFactor4 - (SF4)
* y - the class of the bean. It can be any of BARBUNYA, SIRA, HOROZ, DERMASON, CALI, BOMBAY, and SEKER.


---


## Technologies and algorithms used

### algorithms

* Random Forest (Deprecated)
* CatBoostClassifier (Used)
### technologies

* k_folds 
* Bagging
### Feature Engineering and Preprocessing 

* A) qcut Discretize variable into equal-sized buckets based on rank or based on sample quantiles.
* B) LabelEncoder Encode target labels with value between 0 and n_classes-1 the previous Discretized values
  * Compactness
  * Extent
  * Area
  * 

* C) pandas.cut Used cut when you need to segment and sort data values into bins
  * MinorAxisLength
  * ShapeFactor1
  * Solidity
  * roundness
  * Compactness
  * ShapeFactor2
  * ShapeFactor3
  * ShapeFactor4

### Training The Model

Trained using Kaggle CPU


---

## final Score 

* CatBoost f1_score Train:  0.9408
* CatBoost f1_score test:  0.9405


---
## Final result

the first 2 was cheaters that used the real data for submission

[<img src="Final_rank.png">](https://www.kaggle.com/competitions/dry-beans-classification-iti-ai-pro-intake01/discussion/277505)
