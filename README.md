# Neural_Network_Charity_Analysis
Preprocessing Data for a Neural Network Model / Compile, Train, and Evaluate the Model / Optimize the Model

### Overview of Analysis
- Create a binary classifier that is capable of predicting whether applicants will be successful, if funded by Alphabet Soup, with the information on the CSV file filling more than 34,000 organizations that have received funding from Alphabet Soup over many years.

### Results

## Data Preprocessing
1. Target : Either "IS_SUCCESSFUL" is 1 or 0
2. Features : Every Columns except "IS_SUCCESSFUL"
3. Variable removed: 'EIN' and 'NAME'

## Compiling, Training, and Evaluating the Model
1. There were two hidden layers with the first having 80 neurons, and the second containg 30 neurons. Both having the activation functions "ReLU" since we are looking at positive numbers. There was an output layer with the activation function "Sigmoid" since we are looking for the probability between whole numbers 0 and 1. 
2. The target model gave us a 72.4% accuracy rate which did not reach the goal of 75% or higher.

![image](https://github.com/Angel00Michel/Neural_Network_Charity_Analysis/assets/106771574/77366b04-d118-4e6c-85ad-20f03a5a6ad2)

3. A step-by-step in hopes to try and increase model performance:

- Attempt 1: Remove more columns (unwanted variables) : 'EIN','NAME',"AFFILIATION","USE_CASE". This gave us an accuracy of 65.3% (lower than the original model). 
- Attempt 2: Returning to the original model, we reduced the number of bins for APPLICATION_TYPE (putting "Other" lower than 1000 instead of 500) and CLASSIFICATION (putting "Other" lower than 4000 instead of 1880). This gave us an accuracy of 72.4% (on par with the original model). 
- Attempt 3: Picking up off of attempt 2, we increased the number of hidden layers to 4 instead of 2 (with the following number of neurons for each layer repectively from 1 to 4 : 80, 50, 30, 10). This gave us an accuracy of 72.2% (which is up to par with the original model). 

### Summary
- To summarize, this deep learning model is 72.4% accurate (best attempt). This is not ideal of course, since we wanted a 75% accuracy; at minimum. Therefore, this model needs to have some additional changes. Some recommendations I would like to give:
1. Increase the number epochs to the training regiments. (this helped us perform our Final project analysis with much more accurate and intentional outcomes/probabilities. 
2. Increase the number neurons to all layers. 
3. Increase the number of bins, instead of decreasing them.
