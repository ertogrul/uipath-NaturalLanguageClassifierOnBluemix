# UiPAth-robot-using-NLP-service-on-Bluemix
I have built this demo for the invoicing robot of one of my clients. Demo is making a guess whether the invoice should be posted or rejected. The base for the decision is short description text in the invoice. The output is given by classifier sitting on Bluemix and trained with 50 similar invoice descriptions.

The UiPath robot sends a query (curl command) to Bluemix Natural Language Classifier service and gets the response with book/reject suggestion.

![alt text](https://github.com/ertogrul/uipath-NaturalLanguageClassifierOnBluemix/blob/master/nlc-architecture1.png)
![alt text](https://github.com/ertogrul/uipath-NaturalLanguageClassifierOnBluemix/blob/master/nlc-architecture2.png)

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

I have created the demo on Windows 7, UiPath 2018.2.3 , with mintty bash emulator.

I have registered on IBM Bluemix and initiated Natural Language Classifier service. 


### Installing

1 - Install UiPath and Mintty.

2 - Register to IBM Bluemix.

3 - Initiate Natural Language Classifier service. When starting the service follow below procedure (replace  weather_data_train.csv file with opisy-na-fakturach.csv file available on this repo):
```
https://console.bluemix.net/docs/services/natural-language-classifier/getting-started.html#getting-started-tutorial
```
Please find below  a doc section describing all the commands you can send to this service.

```
https://console.bluemix.net/apidocs/natural-language-classifier
```
Then, start the UiPath and submit the robot. It will use 4 power-shell-command* files to submit four curl commands with example descriptions on the invoice. NLC service on Bluemix gets the requests and uses the classifier to get the informtion if the text sugessts tha invoces should be posted or returned.
