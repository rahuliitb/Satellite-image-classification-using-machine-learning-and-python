# Satellite image classification using machine learning and pyhton
Data classification has been an important part of data science and machine learning. It refers to supervised techniques of identifying the most likely category a sample belongs to out of a given list of categories. Interestingly image classification can be approached in two different ways. One way can be to classify an image into one out of a set of categories and the other can be to classify each pixel within an image to one of out of a set of categories.

In satellite image classification, we deal with the second kind. The task is to categorize each pixel in an image in different categories such as build up area, forest, waterbody, etc. Satellite image study is a relevant area under geoinformatics and computer science and its relevance continues to grow as the quality of imagery improves and the need to monitor global changes increases.

## Data sets descriptions
### Deepsat-4 
Airborne data sets with 1 m resolution
Training size: 4 lakh images, 28 X 28 image each with four channel(Red, green, blue and near infrared)
Test size: 1 lakh images, 28 X 28 image each with four channel(Red, green, blue and near infrared)
No. of classes: 4, Barren land, Trees, Grassland and a class that consist of all land cover classes other than rest of three.
### Deepsat-6
SAT-6 consist of total of 405,000 image patches, each of size 28 X 28 with 1 m resoluton
Training size: 28 X 28 X 4 X 32,4000(having 32,4000 training samples of 28 X 28 each with 4 channels)
Test size: 28 X 28 X 4 X 81,000(having 81,000 training samples of 28 X 28 each with 4 channels) 
No. of classes: 6, Barren land, Trees, Grassland, Road, Buildings and Water bodies

 
