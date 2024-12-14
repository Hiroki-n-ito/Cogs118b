# Cogs118b
## Bone Fracture Detection 


## Conclusions

PCA:
We utilized various feature extraction methods, including Local Binary Patterns (LBP), Edge Detection, Histogram of Oriented Gradients (HoG), and Gray Level Co-occurrence Matrix (GLCM), to capture meaningful features from X-ray images. To reduce dimensionality and noise, we applied Principal Component Analysis (PCA) to these features, ensuring the most critical information was retained for classification. By reducing dimensionality with PCA, we aimed to streamline the identification of bone fractures. We then employed different classifiers, including Gaussian, Support Vector Machines (SVM), Decision Trees, Logisitic Regression, and Random Forest to evaluate the accuracy of these features in fracture detection. PCA played a crucial role in improving the performance of the classifiers by removing redundancy and focusing on essential patterns in the data.


Resnet:
Categorizing bone fracture and non-bone fracture datasets, and training it on the larger dataset we had led to very positive results with accuracy in the high 90s. However, it was lacking in areas such as generalizability and was prone to overfitting. For a new model, change some of the hyper parameters as well as incorporating more tests may lead to better results. Overall, the tests with Resnet in terms of categorizing these datasets was very accurate.


CNN: 
The goal of the CNN Resnet model was to create a cnn model trained on our data and to retrain the final layers of Resnet to optimize the model for our use. In this, we saw that due to the various issues that arose surrounding the class imbalance of our data and the general quality of it, retraining the Resnet resulted in very poor results. With the model consistently converging to the largest class, even without the class imbalance, we are led to believe that the data itself was lacking, low quality, or had features too similar to one another to accurately categories the type of fracture.
This is further supported by the test ran utilizing the "animals" dataset. As these results showed a general accuracy of 60~70% without any tuning to this specific data, we believe the fracture data itself was the issue. Moving forward, we would attempt to create synthetic data, or to improve the pre processing of our data
