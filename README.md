# ml-dress-patterns
project for Machine Learning course at Lewis University

For this project, a data set of 15,702 images of dresses from "Image Categorization: Dress Patterns"
(https://www.crowdflower.com/wp-content/uploads/2016/07/dress_patterns.csv) was used to train a machine learning model to be able to classify which of 17 dress patterns was shown in the image. The data were labeled ahead of this project into the
17 classes, such as floral, stripes, polka-dot, plain, or animal. The images were full-color RGB format as png files
stored in a publicly accessible AWS S3 storage location. Also, the images were marked with a red rectangle
around the actual dress in the image, so as to enable filtering out of much of the irrelevant background in the
images.

The jupyter notebook file initally attempted to download and preprocess each file one by one.  As bad files were discovered (black square instead of red, or other anomolies preventing this data preparation, it became apparent it was more efficient to copy all image files to local storage first, and then I could restart the processing after fixing code without having to re-download them each time.

Once the files were processed, the python code saves the resulting array to a file called visionmatrix.npy so we don't need to run the pre-processing again before training.

Much of the code above is commented out, but can be run as needed.  The remaining code is to train and evaluate the model.  

The data are very unbalanced, and this needs to be remedied before a good classification can be done with this code.

See the MachineLearningWeek6-8Project.pdf file for more information and conclusions.
