<h1> Walk Run Classification </h1>

<h2>Ovewview </h2>
The analysis revolves around the classification of physical activities, specifically distinguishing between 'walk' and 'run' based on sensor data. This kind of classification is pivotal in domains such as health monitoring, sports analytics, and interactive applications, where accurately identifying the type of physical activity can lead to meaningful insights and outcomes.

Here's a structured breakdown of the analysis:

<h3> 1.Data Preprocessing: </h3>
The sensor data, potentially from devices like accelerometers or gyroscopes, undergoes preprocessing to ensure quality and consistency. This stage may involve steps like normalization, dealing with missing values, and extracting pivotal features that effectively characterize each activity.

<h3> 2. Model Development: </h3>

A variety of machine learning models are explored to tackle the classification task. The models might range from simpler ones like Logistic Regression to more complex structures like Neural Networks.
These models are trained on a dataset where each data point is tagged with either 'walk' or 'run', making it a supervised learning task.

<h3> 3. Model Evaluation: </h3>

The performance of these models is meticulously evaluated against a separate set of test data.
Critical metrics such as accuracy, precision, recall, and F1-score are calculated for a comprehensive evaluation. These metrics provide a holistic view of the performance, highlighting both strengths and potential areas for improvement.

<h3> 4. Cross-Validation: </h3>

To ensure robustness and generalizability, cross-validation techniques like KFold, StratifiedKFold, and ShuffleSplit are employed.
This process involves partitioning the data into subsets, then iteratively training the models on certain subsets and validating them on others. It's a rigorous method to ensure the models perform consistently across different samples of data.

</h3>5. Performance Summary: </h3>

The analysis provides a detailed summary of the models' performance, particularly spotlighting the models' capability to classify 'walk' and 'run' activities accurately.
For instance, certain models may exhibit extremely high training accuracy and near-perfect performance metrics on the test set, indicating an excellent fit.
The consistency and capability of the models are further substantiated through cross-validation, where mean accuracies remain impressively high across various validation methods.



Further I have utilised savgol Filter to fine-tune model:

<h2>Introduction to Savitzky-Golay Filter</h2>

The Savitzky-Golay filter, a digital filter often used in this context, is utilized to smooth the data and mitigate the noise without considerably distorting the signal. It is particularly adept at preserving features of the signal such as relative maxima, minima, and width, making it suitable for differentiating between 'walk' and 'run' activities based on sensor data. The filter works by fitting successive sub-sets of adjacent data points with a low-degree polynomial by the method of linear least squares. When applied to the dataset, this filter enhances the signal-to-noise ratio without greatly distorting the signal.


<h3>Performance Summary</h3>

The models show remarkable accuracy and consistency:

Logistic Regression Model shows a Training Accuracy of 99.80% and Test Set Accuracy of 100%.
Precision, Recall, and F1-score are at 100% for both classes, indicating perfect classification on the test set.
Cross-Validation Mean Accuracies are consistently high across different validation methods (KFold, StratifiedKFold, ShuffleSplit), all above 99.7%.

<h3>Conclusion </h3>
The models demonstrate highly accurate predictions, with strong consistency across different validation methods. The perfect classification on the test set and consistently high cross-validation scores indicate the models' robustness and reliability in predicting 'walk' and 'run' activities. The application of the Savitzky-Golay filter enhances the data quality, contributing to the models' high performance. The analysis successfully showcases the potential of these models in accurately classifying physical activities, ensuring their applicability in various practical scenarios.