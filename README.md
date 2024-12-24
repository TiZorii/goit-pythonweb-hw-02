### Topic 2: Homework

Today, we will move on to practical work with deploying applications.

You need to clone a FastAPI application, configure it, and run it in a Docker container. After that, you will verify the application’s functionality and ensure successful connection to the database.

---

### Technical Task Description

1. Use the `git clone` command to clone the repository from [https://github.com/GoIT-Python-Web/FullStack-Web-Development-hw2](https://github.com/GoIT-Python-Web/FullStack-Web-Development-hw2). Navigate to the cloned directory.

2. Create a `Dockerfile` with instructions for building the Docker image for the application.

3. Write a `docker-compose.yaml` file with configurations for the application and PostgreSQL.

4. Use Docker Compose to build the environment and run it using the `docker-compose up` command.

---

💡 **Hint**:  
Make changes to the database connection string `SQLALCHEMY_DATABASE_URL`. It is located in the file `\\conf\\db.py`. Replace `localhost` with the name of the PostgreSQL service from your `docker-compose.yaml` file.  

When using Docker Compose, each service (container) has its own network, and they usually cannot communicate with each other using `localhost`. Instead, you need to use the service name as the hostname.

---

### Step 5: Test the Application's Functionality and Database Availability

💡 **Hint**:  
After starting the container with the application, the browser should display the following:  

**Expected View in Browser:**  

If everything is correctly configured in the `docker-compose.yaml` file, clicking the "Check DB" button should show the following:  

**Expected Database Check Result:**  

If instead of "Welcome to FastAPI!" you see a red error message, it means that your `docker-compose.yaml` file is incorrectly configured.

