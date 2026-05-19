# IoT-Assignment-1

# Real Time Streams Processing With Kafka, Faust and Machine Learning.

Dataset used: Bike Sharing (UC Irvine, Machine Learning Repository, https://archive.ics.uci.edu/dataset/275/bike+sharing+dataset)

Machine Learning Model: RandomForestRegressor (100 Decision Trees). Following are the model performance metrics:

Out-of-Bag Score: 0.9435871930677215
Mean Squared Error: 1770.8210336247462
R2 Score: 0.9440771188850473

## How to Setup

First download all the files from the latest release. You need python 3.11 to run this project without any issues. You can create a virtual environment venv on either VS Code or PyCharm. Then install the dependencies using the command on the terminal pip install -r requirements.txt. After that you need to create a Cluster on Confluence and create the following 3 topics manually: bike-input, predictions, streams_processor-__assignor-__leader. Then generate API keys and get the Bootstrap Server, API Key and API Secret and replace the ones on the code with them. Now, you are all set. First, run python train_model.py to train the model. Then on 3 separate terminal windows first start the streams processing with the command: faust -A app worker -l info, then on the second window start the consumer with: python consumer.py and finally the producer with: python producer.py.

## Demo

https://www.youtube.com/watch?v=x7KFO6m54C0 
