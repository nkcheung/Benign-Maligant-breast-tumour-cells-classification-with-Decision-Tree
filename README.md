# Decision-Tree-for-breast-tumour-cells
Classifies breast tumour into benign or malignant cells based of features of the cell nucleus

## Dataset

Breast Cancer Wisconsin (Diagnostic) Data Set from Kaggle. Features are computer from a digitized image of a fine needle aspirate (FNA) of a breast mass

Ten real-valued features are computerd for each cell nucleus:

radius (mean of distances from center to points on the perimeter) b) texture (standard deviation of gray-scale values)
perimeter
area
smoothness (local variation in radius lengths)
compactness (perimeter^2 / area - 1.0)
concavity (severity of concave portions of the contour)
concave points (number of concave portions of the contour)
symmetry
fractal dimension ("coastline approximation" - 1)
The mean, standard error and "worst" or largest (mean of the three largest values) of these features were computed for each image, resulting in 30 features. For instance, field 3 is Mean Radius, field 13 is Radius SE, field 23 is Worst Radius.

## Statistics generated from Watson Analytics

Desision rules with respective predictive strength(the number is the number of records):

1. Malignant

![malignant](https://user-images.githubusercontent.com/44185972/50152152-dbda2980-02fd-11e9-8041-f5fb07cb935e.png)

2. Benign

![benign](https://user-images.githubusercontent.com/44185972/50152173-e694be80-02fd-11e9-9a2e-178e56ab6cbc.png)

**Due to the high predictive strength of these features, a decision tree is used**

Alhough some features have 100% predictive strength, they are not sufficient to build the decision tree. For instance, even though perimeter_worst>133.5 has 100% predictive strength in predicting malignancy, it does not include all malignant cells as some maliganant cells do not have perimeter_worst>133,5

Feature selection for the decision tree is carried out to select appropriate features for the decision tree.

**Diagnostic strengths of different features:**

91% perimeter_worst
concave points_mean
area_worst
90% concave points_worst
90% radius_worst
88% concavity_mean
87% perimeter_mean
86% radius_mean
86% area_mean
86% area_se
84% concavity_worst
80% radius_se
80% perimeter_se
79% compactness_mean
78% compactness_worst
73% texture_mean
73% concave points_se
72% texture_worst
72% smoothness_worst
71% symmetry_worst
71% concavity_se
70% fractal_dimentsion_worst
69% compactness_se
67% smoothness_mean
67% symmetry_mean
63% fractal_dimension_mean
63% fractal_dimention_se
Features with diagnostic strength of 60% or above are selected
