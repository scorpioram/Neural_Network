Hello Sir/Madam, 

Here is the step by step guide on the Neural Network project.The complete project is divided into multiple sections:

Section 1 : 

Data Pre-Processing and reviewing the data:
    1. We read the Data from H5 file and load them on to training set, Validation set and test set.
    2. Flatten the dataset.
    3. Normalise the dataset
    4. Convert output labels to onehot encoding.
    5. Visualizing the images.

Section 2:

    1. Create Single layered Model and Multi Layered Model.
    2. Train them with 500 epoch.
    3. Compare the training accuracy, validation accuracy, test accuracy.
    4. Plot Learning curve and Accuracy


Section 3:

    1. Using Multi layered Model Train 500 epoch with batch size 8,16,32,64,128,256,512,1024,2048.
    2. Compare the training accuracy, validation accuracy, test accuracy.
    3. Plot Learning curve and Accuracy

Section 4: 

    1. Using Grid search find the best Weight Initializer.

Section 5: 

    1. Using Grid search find the best Optimizer.

Section 6:

    Sanity Checks:
	1> Look for correct loss at chance performance.
	   For example, for CIFAR-10 with a Softmax classifier we would expect the initial loss to be 2.302, 
           because we expect a diffuse probability of 0.1 for each class (since there are 10 classes), and 
           Softmax loss is the negative log probability of the correct class so: -ln(0.1) = 2.302. 
           This Dataset is similar, we would expect the initial loss to be 2.302

        2> As a second sanity check, increasing the regularization strength should increase the loss.

        3> Overfit a tiny subset of data.
	
	4> Train with small learning rate and plot the learning curve.

	5> Train with large learning rate and check loss explodes

Section 7: 

    Coarse Search:
	1> Train 100 iterations with Learning rate between [1e4 to 1e-7] and lambda between [1e-5,1e5]
        2> Review the top models.
        3> Plot top 3 models.

Section 8: 

    Fine Search:
	1> Train 100 iterations with Learning rate between [1e-3 to 1e-2] and lambda between [1e-5,1e2]
        2> Review the top models.
        3> Plot top 3 models.
	4> Re-run the top 3 models with momentum 0.0,0.2,0.6 and 0.9
	5> Plot the top 3 model with momentum.
	6> Plot confusion matrix with the top model.
	7> predict test set and Visualize 10 images and classes.

Section 9:
	Batch Normalization
	1> Create Batch Normalization model.
	2> Train the model and compare with multi layed model and batch normalized model.
	3> Plot the learning curve
	4> Run the batch normalized model with best hyper parameter found in section 8.


Section 9:
	Batch Normalization and Dropout
	1> Create Batch Normalization with Dropout model.
	2> Train the model and compare with multi layed model, batch normalized model and Batch Normalization with Dropout model.
	3> Plot the learning curve
	4> Run the batch normalized model with best hyper parameter found in section 8.

