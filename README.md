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
Guidelines to add your own scripts / modules- Lets understand the projects structure first-

JarvisAI:.
├───configs
├───features
│   ├─── date_time
│   │   └───...
│   └───weather
│       └───...
└───...
4.1. All these above things are folders. Lets understand-

JarvisAI: Root folder containing all the files

features: All the features supported by JarvisAI. This 'features' folder contains the different modules, you can create your own modules. Example of modules- "weather", "setup". These are the two folders inside 'features' directory.

__ init__.py: You need to run this file to test it during the production.

4.2. You can create your own modules in this 'features' directory.

4.3. Let's create a module and you can learn by example-

4.3.1. We will create a module which will tell us a date and time.

4.3.2. Create a folder (module) name- 'date_time' in features directory.

4.3.3. Create a python script name- 'date_time.py' in 'date_time' folder.

4.3.4. Write this kind of script (you can modify according to your own script). Read comments in script below to understand format-

'features/date_time/date_time.py' file- Make sure to add docs / comments. Also return value if necessary.

 import datetime  

 def date():  
     """  
     Just return date as string  :return: date if success, False if fail  
     """  
     try:  
         date = datetime.datetime.now().strftime("%b %d %Y")  
     except Exception as e:  
         print(e)  
         date = False  
 	return date  
   
   
 def time():  
     """  
 	Just return date as string  :return: time if success, False if fail  
 	"""
 	try:  
         time = datetime.datetime.now().strftime("%H:%M")  
     except Exception as e:  
         print(e)  
         time = False  
 	 return time


 # you can run and test your script by calling from main
 if __name__ == '__main__':
     response = date()
     print(response)
     response = time()
     print(response)

4.3.4. Integrate your module to Jarvis AI-

Open JarvisAI\JarvisAI\__init__.py

Format of this py file-

# import custom features
try:
	import features.date_time.date_time
except:
	from .features.date_time import date_time

# integrate your features
class JarvisAssistant:  
    def __init__(self):  
        pass
	def tell_me_date(self):  
		return date_time.date()  
		  
	def tell_me_time(self):  
		return date_time.time()

# test your features from main
if __name__ == '__main__':  
    obj = JarvisAssistant()		
    res = obj.tell_me_time()  
	print(res)
	res = obj.tell_me_date()
	print(res)

4.4. That's it, if you applied all the things as per as guidelines then now just run __ init__.py it should works fine.

4.5. Push the repo, we will test it. If found working and good then it will be added to next PyPi version.

Next time you can import your created function from JarvisAI Example: import JarvisAI.tell_me_date
