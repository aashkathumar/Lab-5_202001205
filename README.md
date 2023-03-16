# **IT - 314 Software Engineering Lab 5**
### **Lab 5 : Static Analysis**<br>
### **Student Name: Aashka Arvindbhai Thumar**<br>
### **Student ID: 202001205**
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - 
### **Topic: Static Analysis**<br>
### **Tool: Mypy**
### **Steps to analyze:**
  1. Install Mypy using the command "pip install mypy" on windows command prompt<br>
  2. Go to the location of the folder in which your files are using the command "cd name_of_location"
  3. To check a file use the command "py -m mypy file_name.py"
  4. We shall now be able to view errors if any<br>
  
**github repo:** https://github.com/omab/python-social-auth<br>
Analysing the files in the folder named "social"<br>

Tool Installation
![205_1](https://user-images.githubusercontent.com/75677392/225571417-a0a61c42-a27d-4b3d-9b00-af290323092a.png)

1. Checking "https://github.com/omab/python-social-auth/blob/master/social/p3.py"
![205_2](https://user-images.githubusercontent.com/75677392/225571876-0e6b98d2-d793-4bde-9719-eea9d10db44b.png)

2. Checking "https://github.com/omab/python-social-auth/blob/master/social/store.py"
![203_4](https://user-images.githubusercontent.com/75677392/225573021-235de036-3efb-4f86-abef-40e91db1fa55.png)

### **Analyzing the errors**
1. error: Library stubs not installed for "six" (or incompatible with Python 3.10)<br>
This error is caused as the types-six environment is missing. This may be resolved  after installing types-six to the development environment by using the command "pip install types-six"<br>
2. error: Cannot find implementation or library stub for module named "social_core.store"<br>
Mypy uses it's own search path for imports and does not resolve them like how Python does. Hence it is not able to detect the social_core.store module.
