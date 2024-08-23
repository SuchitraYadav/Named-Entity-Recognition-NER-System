# Custom Named Entity Recognition (NER) Model with spaCy
This project demonstrates the process of training a custom Named Entity Recognition (NER) model using the spaCy library. The model is designed to identify specific entities like MEDICINE, MEDICALCONDITION, and PATHOGEN in medical text data.

## Project Overview
The goal of this project is to train a custom NER model that can accurately identify and classify various medical entities within text data. 

The process includes:
* Data Preparation: Loading and transforming annotated data into a format suitable for training.
* Training the Model: Using spaCy to train a NER model with the prepared data.
* Model Evaluation: Testing the model's performance on a separate dataset and calculating key evaluation metrics.
* Visualization: Visualizing the model's predictions on sample texts.


## 1. Loading the spaCy Model
Purpose: Load the pre-trained en_core_web_lg spaCy model, which is a large English language model containing word vectors and NER capabilities. This model serves as a foundation, which can be further trained on specific custom entities.
  
## 2. Loading and Inspecting Annotated Data
Load a JSON file containing annotated data for training. The data is in a format where each example contains text and annotations for entities like MEDICINE, MEDICALCONDITION, and PATHOGEN.

## 3. Data Transformation
Convert the JSON data into a format that spaCy can use for training. Each training example consists of the text and the positions of entities within the text.

## 4. Label Extraction
Identify all unique entity labels in the dataset. Ensures that the model knows all the entity types it needs to classify.

## 5. Creating a spaCy DocBin Object for Training
Transform the training data into spaCy's DocBin format, which is more efficient for training. It ensures no overlapping entities, which can confuse the model during training.

## 6. Configuring and Training the Model
Use spaCy’s command-line tools to auto-fill the configuration file and train the model.
* Configuration: The base_configg.cfg is a template that is filled with necessary parameters for training.
* Training Output: The model is saved in the model-last directory after training.

## 7. Testing and Visualizing the Model
Load the best-trained model and test it on a sample text. Use displacy.render to visualize the entities with custom colors.

## 8. Model Evaluation
Evaluate the trained model on unseen test data to measure its precision, recall, and F1-score. These metrics help determine the effectiveness of the model.

## Conclusion
This project illustrates how to build a custom NER model using spaCy. The model can accurately detect and classify medical-related entities in text data, which is crucial in fields like healthcare and biomedical research.

## Future Work

* Expand the dataset: Incorporate more diverse and complex examples.
* Fine-tuning: Experiment with different configurations to further improve model accuracy.
* Deployment: Integrate the model into a web application using Flask or Django for real-time NER tasks.
