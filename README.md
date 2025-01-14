# Django Questions

<img src="./images/0_5mCMOCogRI-yzfUM.gif" alt="Picture" width="auto" height="auto">

## What is the difference between Flask and Django?

<img src="./images/Flask-vs-Django.png" alt="Picture" width="auto" height="auto">

| Feature               | Flask                                     | Django                           |
|-----------------------|-------------------------------------------|----------------------------------|
| **Type**              | Microframework                            | Full-stack framework             |
| **Complexity**        | Lightweight, minimalistic                 | More complex, batteries-included |
| **Flexibility**       | High (you choose components)              | Low (comes with built-in tools)  |
| **Database Support**  | No built-in ORM                           | Built-in ORM (Django ORM)        |
| **Admin Interface**   | Not included                              | Built-in admin interface         |
| **Learning Curve**    | Easier for beginners                      | Steeper learning curve           |
| **Use Case**          | Small to medium projects                  | Large, complex projects          |
| **Template Engine**   | Jinja2 (default)                          | Django Template Language         |
| **REST API Support**  | Requires extensions (e.g., Flask-RESTful) | Built-in (Django REST Framework) |
| **Community**         | Large, but smaller than Django            | Very large and mature            |

## What is Django?

- Django is python based web deveolpment Framwork.
- Free and Open-source.
- comes with ready-to-use features like login system, database connection and CRUD operations.

## How does Django Work?

**Django follows the MVT design pattern (Model View Template).**

- Model: The data you want to present, usually data from a database.
- View: A request handler that returns the relevant template and content based on the request from the user
- Template: A text file (like an HTML file) containing the layout of the web page, with logic on how to display the  data.

<img src="./images/1_XohhamnRotq53fQaY5HQfA.png" alt="Picture" width="auto" height="auto">

**Model**

- In Django, the data is delivered as an Object Relational Mapping (ORM), which is a technique designed to make it   easier to work with databases.
- The most common way to extract data from a database is SQL. One problem with SQL is that you have to have a pretty good understanding of the database structure to be able to work with it.
- Django, with ORM, makes it easier to communicate with the database, without having to write complex SQL statements.
- The models are usually located in a file called `models.py.`

<img src="./images/models.png" alt="Picture" width="auto" height="auto">

**View**

- A view is a function or method that takes http requests as arguments, imports the relevant model(s), and finds out what data to send to the template, and returns the final result.
- The views are usually located in a file called `views.py.`

<img src="./images/views.png" alt="Picture" width="auto" height="auto">

**Template**

- A template is a file where you describe how the result should be represented.
- Templates are often `.html` files, with HTML code describing the layout of a web page, but it can also be in other file formats to present other results, but we will concentrate on `.html` files.
- Django uses standard HTML to describe the layout, but uses Django tags to add logic:

<img src="./images/template.png" alt="Picture" width="auto" height="auto">
**URLs**

- Django also provides a way to navigate around the different pages in a website.
- When a user requests a URL, Django decides which view it will send it to.
- This is done in a file called `urls.py.`

<img src="./images/url.png" alt="Picture" width="auto" height="auto">

## How MVT pattern Django's approach work under the hood?

1. Django receives the URL, checks the `urls.py` file, and calls the view that matches the URL.
2. The view, located in `views.py`, checks for relevant models.
3. The models are imported from the `models.py` file.
4. The view then sends the data to a specified template in the `template` folder.
5. The template contains HTML and Django tags, and with the data it returns finished HTML content back to the browser.

## What is Virtual Environment ?

<img src="./images/python-virtual.png" alt="Picture" width="auto" height="auto">

- A virtual environment is a tool that helps to keep dependencies required by different projects separate by creating isolated Python virtual environments for them. This is one of the most important tools that most Python developers use.

### Why do we need a virtual environment?
- Creating a Python virtual environment allows you to manage dependencies separately for different projects, preventing conflicts and maintaining cleaner setups. With Python’s venv module, you can create isolated environments that use different versions of libraries or Python itself.

## How to Create a Django Project

1. **First, create a directory for the project:**

   <img src="./images/1.png" alt="Picture" width="auto" height="auto">

   - Use the following command to create a directory:
     ```bash
     mkdir first_project
     ```
   - Navigate into the directory:
     ```bash
     cd first_project
     ```

---

2. **Set up a virtual environment:**

   <img src="./images/2.png" alt="Picture" width="auto" height="auto">

   - Create a virtual environment using:
     ```bash
     python -m venv env
     ```
   - If you encounter issues, install `virtualenv` globally:
     ```bash
     pip install virtualenv
     ```
     Then, try creating the virtual environment again.

---

3. **Activate the virtual environment:**

   <img src="./images/3.png" alt="Picture" width="auto" height="auto">

   - On macOS/Linux:
     ```bash
     source env/bin/activate
     ```
   - On Windows:
     ```bash
     env\Scripts\activate
     ```

---

4. **Install Django:**

   <img src="./images/4.png" alt="Picture" width="auto" height="auto">

   - Use `pip` to install Django:
     ```bash
     pip install Django
     ```

---

5. **Create a Django project:**

   <img src="./images/5.png" alt="Picture" width="auto" height="auto">

   - Use the `django-admin` command to create a new project:
     ```bash
     django-admin startproject login_system
     ```
     - **`django-admin`**: Django’s command-line utility for administrative tasks.
     - **`startproject`**: The command to create a new Django project.
     - **`login_system`**: The name of your project.

---

6. **Navigate into the project directory:**

   - Move into the newly created project directory:
     ```bash
     cd login_system
     ```

---

7. **Run the development server:**

   <img src="./images/6.png" alt="Picture" width="auto" height="auto">

   - Start the Django development server:
     ```bash
     python manage.py runserver
     ```

---

8. **Verify the project:**

   - Open your browser and navigate to:
     ```
     http://127.0.0.1:8000/
     ```
   - If everything is set up correctly, you should see the Django welcome page:

     <img src="./images/0_5mCMOCogRI-yzfUM.gif" alt="Picture" width="auto" height="auto">

---
