# MHH Chatbot

This project is a simple AI chatbot named "MHH", which uses a trained deep learning model to respond to various user inputs. The chatbot is designed to handle multiple intents and respond accordingly based on a predefined set of patterns and responses.

## Project Structure

- **intents.json**: This file contains the different intents that the chatbot can recognize, along with associated patterns (phrases) and responses.
- **chatbotmodel.h5**: The trained model file saved in HDF5 format.
- **words.pkl**: A pickle file containing the list of all words used in the patterns after tokenization and lemmatization.
- **classes.pkl**: A pickle file containing the list of classes (intents) recognized by the chatbot.
- **training.py**: The Python script used for training the chatbot model.
- **chatbot.py**: The main script to run the chatbot.

## Dependencies

The project requires the following Python libraries:

- `tensorflow`
- `nltk`
- `numpy`
- `json`
- `pickle`

You can install the required libraries using the following command:<br>

<b>pip install tensorflow nltk numpy</b>

## Training the Model
To train the chatbot model, run the training.py script. This script will:

Load the intents from intents.json.
Tokenize and lemmatize the patterns.
Create a bag of words and corresponding output vectors for training.
Define and compile a Sequential model.
Train the model with the training data.
Save the trained model as chatbotmodel.h5 along with words.pkl and classes.pkl.
<b>python training.py</b>

## Running the Chatbot
Once the model is trained, you can run the chatbot using the chatbot.py script. This script will:

Load the trained model and required data files (words.pkl, classes.pkl).
Tokenize and lemmatize user input.
Predict the intent of the user input based on the trained model.
Return a response based on the predicted intent.
<b>python chatbot.py</b>

## Example Interaction
<b>User:</b> Hello<br>
<b>Bot:</b> Hello!<br>

<b>User:</b> How old is Sameer?<br>
<b>Bot:</b> My creator Sameer is 20 years old.

## Intents
The chatbot can recognize and respond to the following intents:

**greetings:** Responds to general greetings like "hello", "hi", etc.<br>
**goodbye:** Responds to farewell messages like "bye", "see you later", etc.<br>
**age:** Responds to questions about Sameer's age.<br>
**name:** Provides the name of the chatbot.<br>
**shop:** Placeholder for shopping-related queries (currently not implemented).<br>
**hours:** Provides the operating hours of the chatbot (24/7).<br>
**kpop:** Shares the chatbot's favorite K-pop group, which is NewJeans.<br>

## Customization
**Adding New Intents:** You can add new intents to the intents.json file by adding new entries under the intents array. Make sure to retrain the model after adding new intents.<br>
**Modifying Responses:** You can change the responses in the intents.json file. No need to retrain the model for response changes.

## Acknowledgments
The chatbot is inspired by the NewJeans K-pop group, and its name "MHH" is based on the initials of members Minji, Haerin, and Hanni.
