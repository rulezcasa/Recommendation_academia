# About

Aiming to bridge the gap between academic collaboration and networking with the help of a swipe based recommendation algorithm. The model is integrated into a mobile application through which users can seek collaborations with like minded individuals.  

# Directory structure
- Jupyter
  - NLP-responses.ipynb (Jupyter notebook file)
- Flask-app
  - app.py (API)
  - module.py (NLP model)
- -README.MD (Containing specifcs of the application)
- requirements.txt (Depedencies required to run the app)
 

# Development and tools

## Tech stack :

Frontend : Flutter

API : Flask

Backend : Python 

Database : MongoDB

## Login page :
*Components*

1. Email input box
2. Password input box
3. Submit button (POST)

&nbsp;

*API reference*

```http (POST)
  https://dh-oyl4.onrender.com/login
```

| Parameter | Return Type     | Return Object                  |
| :-------- | :------- | :-------------------------------- |
| `if logged in`      | `json` | {”authentication”: True}|
| `else`      | `json` | {”authentication”: False}|



## Sign up page:

*Components*

1. Email input box
2. Password input box
3. Repeat password input box
4. Name input box
5. Profession dropdown menu :
    - Student
    - Faculty
    - Working professional
6. Year of study (If student) dropdown menu :
    - Year 1
    - Year 2
    - Year 3
    - Year 4
7. Interest drop down menu :
    - Projects
    - Research work
    - Group study
8. Collaboratoin with
    - Student
    - Faculty
    - Working professional
9. Topic of collaboration input box
10. User’s skillset input box
11. Experience (If professional) number menu 
12. Submit button (POST)

&nbsp;

*API reference*

```http (POST)
  https://dh-oyl4.onrender.com/signup
```

| Parameter | Return Type     | Return Object                      |
| :-------- | :------- | :-------------------------------- |
| `If email already exists`      | `json` | {"signup":"exists"} |
| `elseif password mismatch`      | `json` | {"signup":"mismatch"} |
| `else`      | `json` | {"signup":"success"} |


## Retrieving user data :

&nbsp;
*API reference*

```http (GET)
  https://dh-oyl4.onrender.com/get_data?email=$email
```

Replace $email with actual email or pass as parameter to function

| Parameter | Return Type     | Return Object                  |
| :-------- | :------- | :-------------------------------- |
| `if email found`      | `json` | all the details|
| `else`      | `json` | {”data”: 'Data not found for the given email'}|




