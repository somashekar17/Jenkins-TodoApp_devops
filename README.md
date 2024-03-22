# django-todo
A simple todo app built with django

![todo App](https://raw.githubusercontent.com/shreys7/django-todo/develop/staticfiles/todoApp.png)
### Setup
To get this repository, run the following command inside your git enabled terminal
```bash
 git clone https://github.com/somashekar17/django-todo.git
```
You will need django to be installed in you computer to run this app. Head over to https://www.djangoproject.com/download/ for the download guide

Once you have downloaded django, go to the cloned repo directory and run the following command

Now change the directory using this command

```bash
cd djnago-todo
````

Here you will the get command for mirgrations.

```bash
 python manage.py makemigrations
```

This will create all the migrations file (database migrations) required to run this App.

Now, to apply this migrations run the following command
```bash
 python manage.py migrate
```

One last step and then our todo App will be live. We need to create an admin user to run this App. On the terminal, type the following command and provide username, password and email for the admin user
```bash
 python manage.py createsuperuser
```

That was pretty simple, right? Now let's make the App live. We just need to start the server now and then we can start using our simple todo App. Start the server by following command

```bash
 python manage.py runserver
```

Once the server is hosted, head over to http://127.0.0.1:8000/todos for the App.

Till now we did execute in our local machine,

# Now we are going to Deploy this project in AWS EC2.

First we will create a new AWS EC2 Instance:

follow the steps to create EC2 Instance:

## 1.  Click on the Lunch Instances.


![AWS First ](https://github.com/somashekar17/TodoApp_devops/assets/49157790/3ded636d-03a7-44d2-9643-2196d1fd0362)


## 2. Give a new name for EC2 instance and Select the OS and select the free eligible AMI for this Instance.


   ![AWS second](https://github.com/somashekar17/TodoApp_devops/assets/49157790/b3bdb6d9-aae3-4ae0-abfd-8cf2863b0f63)


## 3. Now Select the Instance type ( RAM, CPU, Memory) it should be free.


![AWS third](https://github.com/somashekar17/TodoApp_devops/assets/49157790/5748498b-79b7-4989-97d2-5a0fee714908)


## 4. Now you need to create a new key pair for security.

   
![AWS Fourth](https://github.com/somashekar17/TodoApp_devops/assets/49157790/f2848435-6301-4c16-9c82-f31a4f44d70d)


## 5.Now, choose the security group and ensure all boxes are selected. This ensures that in the future, you won't encounter any errors when accessing the instance from anywhere in the world. Finally, click on "Launch Instance".


![AWS Fivth](https://github.com/somashekar17/TodoApp_devops/assets/49157790/6330253b-1521-41c7-9d9d-364423ee2af4)


## 6. Your instance will take 2- 3 mintues to create.

  ![AWS Sixth](https://github.com/somashekar17/TodoApp_devops/assets/49157790/59e86912-f8a9-4ad6-9e5b-37f64ef58413)


## 7. Now, Click on the instance and copy the "Public IP address"  or " Connect" .


![AWS 7](https://github.com/somashekar17/TodoApp_devops/assets/49157790/bea99709-3e81-4578-815a-a6699dd01e59)

     

## 8. Copy the "ssh -i "security pair-key" ubuntu@1.2.3.4

   
![AWS 8](https://github.com/somashekar17/TodoApp_devops/assets/49157790/98831a6f-721f-4210-8bca-5378350daedc)



## 9. Copy and paste command in terminal.


   ![AWS 9](https://github.com/somashekar17/TodoApp_devops/assets/49157790/2e1cf74b-f74c-4ef0-9467-0d157a3b1109)


## 10. Now, you have inside the Instance and create a new directory.


![AWS 10](https://github.com/somashekar17/TodoApp_devops/assets/49157790/86894156-7ae3-462f-9c5f-857495814a8b)


## 11. After Directory creation, Clone the repo and change the dir to djnago-todo.


![AWS 11](https://github.com/somashekar17/TodoApp_devops/assets/49157790/f77206ed-bc84-47c2-8a07-8450ebe870dd)


## 12. Now use this command to run this application.
```bash
 python3 manage.py makemigrations
```
```bash
 python3 manage.py migrate
```
```bash
 python3 manage.py createsuperuser
```
## 13. This is final command to run your application in internet and give this IP address to access this application any where from the world.
 ```bash
 python3 manage.py runserver 0.0.0.0:8000
```
