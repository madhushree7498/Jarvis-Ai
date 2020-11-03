# Jarvis-Ai
Jarvis AI is a Chatbot, Assistant and more
1. What is Jarvis AI-
Jarvis AI is a Python Module which is able to perform task like Chatbot, Assistant etc. It provides base functionality for any assistant application. Well, you can contribute on this project to make it more powerful.
2. Prerequisite-
To use it only Python (> 3.6) is required.
To contribute in project: Python is the only prerequisite for basic scripting, Machine Learning and Deep Learning knowledge will help this model to do task like AI-ML. Read How to contribute section of this page.
3. Getting Started (How to use it)-
Install the latest version-
pip install JarvisAI

It will install all the required package automatically.

If anything not install then you can install requirements manually. pip install -r requirements.txt The requirementx.txt can be found here.
Usage and Features-
After installing the library you can import the module-

import JarvisAI
obj = JarvisAI.JarvisAssistant()
response = obj.mic_input()
print(response)
Commands and features-
The functionality is cleared by methods name. You can check the code for example. These are the names of available functions you can use after creating JarvisAI's object-

mic_input
text2speech
shutdown
website_opener
send_mail
tell_me_date
tell_me_time
launch_any_app
weather
news
tell_me
datasetcreate (It will create face dataset)
face_recognition_train (It will train the TF Keras Model based on CNN)
predict_faces (Predict real-time faces)
