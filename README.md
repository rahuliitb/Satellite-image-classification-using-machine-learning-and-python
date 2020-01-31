# Satellite image classification using machine learning and pyhton
Data classification has been an important part of data science and machine learning. It refers to supervised techniques of identifying the most likely category a sample belongs to out of a given list of categories. Interestingly image classification can be approached in two different ways. One way can be to classify an image into one out of a set of categories and the other can be to classify each pixel within an image to one of out of a set of categories.

In satellite image classification, we deal with the second kind. The task is to categorize each pixel in an image in different categories such as build up area, forest, waterbody, etc. Satellite image study is a relevant area under geoinformatics and computer science and its relevance continues to grow as the quality of imagery improves and the need to monitor global changes increases.

## Data sets descriptions
### Deepsat-4 
  1. Link to downlaod data set https://www.kaggle.com/crawford/deepsat-sat4
  2. Airborne data sets with 1 m resolution
  3. Training size: 4 lakh images, 28 X 28 image each with four channel(Red, green, blue and near infrared)
  4. Test size: 1 lakh images, 28 X 28 image each with four channel(Red, green, blue and near infrared)
  5. No. of classes: 4, Barren land, Trees, Grassland and a class that consist of all land cover classes other than rest of    three.
### Deepsat-6
  1. Link to download data set https://www.kaggle.com/crawford/deepsat-sat6
  2. SAT-6 consist of total of 405,000 image patches, each of size 28 X 28 with 1 m resoluton
  3. Training size: 28 X 28 X 4 X 32,4000(having 32,4000 training samples of 28 X 28 each with 4 channels)
  4. Test size: 28 X 28 X 4 X 81,000(having 81,000 training samples of 28 X 28 each with 4 channels) 
  5. No. of classes: 6, Barren land, Trees, Grassland, Road, Buildings and Water bodies
## Feature Extraction

The feature extraction phase computes 18 features from the input imagery. The key feature that we use for classification are Haralick texture that includes energy, correlation, entropy, contrast, 2nd moment, varaince, co-variance, mean, etc., and sum of variance of hue, saturation, intensity. Haralick texture is used to quantify an image based on texture and fundamental concept involved in computing Haralick texture features is the Gray Co-occurrence matrix or GLCM. You can read about it in detail here http://haralick.org/journals/TexturalFeatures.pdf.

Since, two of the classes in SAT-4 and SAT-6 are trees and grasslands, we incorporate features that are useful determinants for segregation of vegetated areas from non-vegetated ones. The red band already provides a useful feature for discrimination of vegetated and non-vegetated areas based on
chlorophyll reflectance, however, we also use derived features (vegetation indices derived from spectral band combinations) that are more representative of vegetation greenness - this includes the Normalized Difference Vegetation Index (NDVI) and Atmospherically Resistant Vegetation Index.

                              NDVI=(NIR band-RED band)/(NIR band-RED band)
                              ARVI= (NIR band-(2 X RED band -BLUE band))/(NIR band-(2 X RED band + BLUE band))
