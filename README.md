# Charity-Funding-Predictor (module 21)
This project is the first of mine to utilize Neural Networks to try and make accurate predictions of the data and resources.

**concepts utilized on the project: ** <br />
<ul>
<li>Jupyter Notebook</li>
<li>Pandas</li>
<li>Cleaning and standardizing data in order for it to be processed by a Neural Network</li>
<li>Accessing and improving layers of a Neural Network</li>
<li>Analyzing results of Neural Networks and make recommendations </li>
</ul>


<h1>REPORT </h1>

**Overview of the analysis: Explain the purpose of this analysis.** <br />
  The overview of this project was to determine what variables influence the result of a Charity Fund. The given resources was a csv of tens of thousands of 
  fundraisers, with certain variables (asked, raised, private/public, company/independent, etc.)

Results: Using bulleted lists and images to support your answers, address the following questions.




<h2> Data Preprocessing </h2>

**What variable(s) are the target(s) for your model?** <br />
  the target for the model is to predict if a fundraiser will be successful or not depending on its variables. binary: yes (1), no(0) <br />

**What variable(s) are the features for your model? ** <br />

  features are the variables that determine if the fundraiser will be successful, ask, raised, type, etc. <br />

**What variable(s) should be removed from the input data because they are neither targets nor features? ** <br />

  variables that should be removed are ones that do not influence the data/model at all, such as strings, or in this case the names of the fundraisers and the 
  EIN (serial number). <br />


<h2> Compiling, Training, and Evaluating the Model </h2>

**How many neurons, layers, and activation functions did you select for your neural network model, and why? **

![image](https://user-images.githubusercontent.com/106775945/201774970-7ea3dfcc-ebf7-42e2-bda8-dd148b88592d.png)

![image](https://user-images.githubusercontent.com/106775945/201775266-9726260d-53a4-43ca-aa85-14f0b04fcad9.png)

![image](https://user-images.githubusercontent.com/106775945/201775276-39d0696d-7ffd-4af4-b30e-d04211422576.png)

The above images show the 3 main models built for the prediction. All Three used 3 layers, with different activations in order to group the data in several different ways through the epoch. 

a relatively higher unit number for the "relu" activation model was optimal because the activation is linear, leaving many different interpretations of the data, while 
the other activations are more binary, making the unit count lower.

Sigmoid and tanh as activations because the data needed to be categorized as many different ways as possible, and using both of them on different layers helped greatly improve the accuracy of the models.





**Were you able to achieve the target model performance? **

The best model built was only 3% lower than the target model performance. Yielding a slightly lower than desired model.


**What steps did you take in your attempts to increase model performance? **

![image](https://user-images.githubusercontent.com/106775945/201776037-d2987c06-49d2-4414-a917-484360e3bf6a.png)

Using a fourth layer was a hypothesis to see if that would increase the accuracy, but the results only got to 50%~ with the addition of the last layer. </br>

Other steps was to experiment with the number of neurons per layer, but those attempts either recreated a similar accuracy, or found negative results





<h2> Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation. </h2>

After trimming the data and building a Neural-Network with several different algorithms, an accuracy of 72.9% has been achieved with the big data prediction. Higher levels of accuracy may be achieved with better configuration of the hidden layers.

I used an activation method for each different layer for the algorithm to apply several different mathematical interpretations of the data for it to potentially increase its accuracy. With the first attempts of the Neural-Network implementation, two hidden layers were used with both using Rectified Linear Unit (relu), yielding an accuracy of 22%. This is because not many different sorting methods were used with the data inside the Neural Network preventing the algorithm from making confident predictions.

After researching more optimal activation models (Sigmoid, Tanh), I implemented them as hidden layers and started to see much more promising results.

Another variable that can be changed to increase the accuracy of the model potentially further is the number of units put into each layer, further fine tuning the model to make accurate predictions. (Very large amounts of units yield lower accurate results)


