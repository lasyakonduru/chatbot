INTRODUCTION 
Chatbots are computer programs built to simulate human conversations— whether on a website, a messaging app, or a virtual assistant. With today’s customers expecting immediacy and personalization in their interactions with brands, the addition of chatbots as a communication channel has become critical to business growth. 

In its simplest form, chatbots can be programmed to answer specific, frequently asked questions, offering an easy way to engage with visitors. On the other hand, Artificial Intelligence (AI) - powered chatbots can learn from user behavior and previous agent interactions to predict visitor behavior and offer relevant information. Chatbots can help automate interactions and offer instant accessibility across sales, marketing, and customer service functions. 

The purpose of a chatbot is to improve the productivity of customer-facing teams and reduce the workload caused by live chat. This can be achieved through training an AI-enabled chatbot to spot patterns, language intent and identify the most appropriate response without human involvement.  

The most outstanding chatbots starting at now are voice chatbots: Alexa and Siri. Nevertheless, chatbots are starting at now being gotten at a high rate on PC talk stages. 

METHODOLOGY: 

CLASSIFICATION OF CHATBOT MODELS: 
1. Result Based:  
Result based model have a primary objective to achieve. They are goal oriented and are developed to address a specific task. 

Chatbots using conversational model are not focused on providing specific information or to address common routine tasks, they are more focused on the general aspect of the conversation. 

Chatbots using task-based model are designed for handling specific scenarios such as setting a reminder, scheduling an event, or helping with troubleshooting. Platforms such as Dialog flow by Google, Wit by Facebook and the Bot Framework by Microsoft exist for building task-based chat bot from scratch. 

 These bots are designed by specifying a set of intents, entities and the resulting action to be performed if the conversation reaches a defined state. Task based model is widely used as they are goal-oriented chat bots focused on helping users accomplish a certain task. Chat bots using task-based model have components such as Natural Language Unit to parse and understand the user's query, Dialog Manager and Dialog Policy to help accomplish the task. 

2. Domain Based: 
Chat bots following open domain model are designed to retrieve information for various open-ended general questions such. These agents are developed using algorithms such as PageRank combined with Natural Language Processing.  

On receiving an open-ended question like "What year was Alan Turing born?”, the chat agent parses the question and identifies important key phrases(tags), and then proceeds to search the database for an answer matching those key tags. Personal assistants such as Siri, Cortana, Alexa and Google Assistant are good examples of chatbots using open domain model where they attempt to return an answer for each task they receive.  

Closed domain agents are domain specific. They operate on information regarding a specific area of interest. These agents are suitable for narrow scenarios like offering information about a tourist site, providing recommendations for a restaurant. Closed domain agents are relatively easy to implement and perform well in real environments. 

3. Response Based: 
Response based agents have a predefined set of questions and their respective answer. Whenever a same or similar question is asked the agent simply responds with the predefined answer or chooses the answer with the highest predicted priority from a set of answers. A dialog flow manager exists in order to choose the most suitable answer for the query.  

Chatbots built using template model generate responses based on predefined templates and patterns. These predefined templates can be defined using Artificial Intelligence Markup Language (AIML). Artificial Intelligence Markup Language is based on XML type schema where the pattern and its response are organized into XML type tags. In combination with Natural Language Processing and rich pattern, AIML can be used to build a smart chat bot. Bots using Template model additionally use a parser to interpret user queries, identify tags and find out which rule matches the user query.  

Search based model is a retrieval-based model which is reliable and easy to build. Retrieval based bots follow the directed flow defined to find the best response. Initially a database of set question tags and answers are populated into the database. on information. As the bot responds to more and more questions it automatically trains itself to rank the response from a set of predefined responses. 


POPULAR CHATBOT IMPLEMENTATION ALGORITHMS:  
Decision Tree Decision tree is a machine learning classification algorithm where a tree-like structure is used to map decisions and their possible consequences. In the late twentieth century major organizations in the telecommunication industry started to implement decision trees in their automated voice-based telephone systems. The conversation is approached logically in stepwise manner to arrive at the right intent (response or action). The root of the tree would be the customer’s initial question. Typically, the goal or action would be at the leaf of the tree structure. Between the root and leaf (intent) lies multiple nodes and branches. Each node represents follow up question (usually a yes/no question) and the branches represent the choices (answer for that question). The major drawback of Decision trees is that it causes over-fitting. To overcome this, more powerful variants of decision trees such as C4.5 and random tree algorithms are used.  

Artificial Neural Networks algorithms by design, try to process information the same way as our brain. Artificial neural networks are a collection of nodes called artificial neurons. The artificial neurons are interconnected and communicate with each other. These neurons are organized into multiple layers starting from input layer which receives external data followed by zero or more in-between hidden layers and an output layer which produces the result. There exist multiple connections between neurons of same or different layers and each connection is assigned a weight that represents its importance. The output is calculated from the input using weighted connections which are calculated from repeated iterations while training the data. Based on the flow of data though the network, Artificial neural networks can be classified into Feed-forward and Feedback. In Feed-Forward networks the flow of information is unidirectional. Feed-back neural network are recurrent networks where feedback loops are allowed. In Feed-back networks, the signal can travel in both directions. Sequence to Sequence (Seq2Seq) is a type of recurrent neural network and is one of the most popular network models for designing machine translation and dialogue systems. Seq2Seq model consists of two recurrent neural networks, an encoder and a decoder. Since recurrent neural networks have the problem of vanishing gradient, much more powerful variants such as Long Short-Term Memory (LSTM) or Gated Recurrent Units (GRU) are used. The encoder network processes the input sentence (user query) by breaking down the sentence into a hidden feature vector consisting of only the important words. The decoder takes as input the hidden vector generated by the encoder. Along with its own hidden states, current word and the hidden vector generated by encoder, the decoder tries to produce the next hidden vector and finally predicts the next word. Thereby, the Seq2Seq model is able to understand the context of the conversation by taking two inputs (one from the user and the other from the previous output of the model) at each point of time.
 
Natural Language Processing provides chatbots the ability to read, understand and derive meaning from human languages. Natural language processing is a collective name for a combination of steps to be followed to convert the customer’s text or speech into a structured data that could be used to select the related response. Some of the steps include segmentation, tokenization, lemmatization, identifying stop words, dependency parsing, named entity recognition and coreference resolution. 

IMPLEMENTATION 

Required packages – All the required packages in python have to be imported. 

Intent - An intent categorizes an end-user's intention for one conversation turn. Defining few simple intents and bunch of messages that corresponds to those intents and also map some responses according to each intent category. For each agent, you define many intents, where your combined intents can handle a complete conversation. When an end-user writes or says something, referred to as an end-user expression, Dialogflow matches the end-user expression to the best intent in your agent. Matching an intent is also known as intent classification. 

Data Preparation -  

A variable like “training_sentences” holds all the training data (which are the sample messages in each intent category) and another “training_labels” variable holds all the target labels correspond to each training data.  

Then we use “Label_Encoder()” function provided by scikit-learn to convert the target labels into a model understandable form. 

Next, we vectorize our text data corpus by using the “Tokenizer” class and it allows us to limit our vocabulary size up to some defined number. When we use this class for the text pre-processing task, by default all punctuations will be removed, turning the texts  

into space-separated sequences of words, and these sequences are then split into lists of tokens. They will then be indexed or vectorized. We can also add a value for “out of token” to deal with out of vocabulary words(tokens) at inference time. 

The “pad_sequences” method is used to make all the training text sequences into the same size. 

Model training - 

Defining Neural Network architecture for the proposed chatbot model and for that we use the “Sequential” model class of Keras.  

The following is the model architecture: 

The “fit” method with training data and labels is called, to train the model. After training, all the required files are saved in order to use it at the inference time. So that we save the trained model, fitted tokenizer object and fitted label encoder object. 

Inference – To check whether the model is working perfectly, the chat function is implemented to engage with the real user. When a new user message is received, the chatbot will calculate the similarity between the new text sequence and training data. Considering the confidence scores got for each category, it categorizes the user message to an intent with the highest confidence score. 

Integrate – The trained chatbot model is integrated with other chat application in order to make it more effective to deal with real world users. 

CONCLUSION: 
A chatbot allows even small and medium businesses to automate customer service live chat conversations. Chatbots in the late 20th century followed basic rules and had no reasoning capability. But with help of technologies such as big data, data mining and artificial intelligence, chat bots are getting smarter day by day. From this study, it becomes clear that natural language processing plays a predominant role in designing a chat bot. Many organizations have adopted to handle some of their customer’s query using open domain model. It has become obvious that chat bots which provides natural open domain conversations ultimately have the potential to enhance the customer experience and thereby reducing organizations dependency on human resources. 
