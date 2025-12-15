## Creating CodecraftHub using the ChatGPT Mini 40 model with example prompts from IBM AI Developer Course (Generative AI: Elevate your Software Development Career)

Prompt 1: Gather requirements for the development of the learning platform
```
I want to create a personalized online learning platform, starting with the server side. Recommend an optimal design and architecture for the backend, and help me gather all the functional and non-functional requirements needed to build it.
```

Prompt 2: Choose the architecture and components
```
I want to use a microservices architecture for the server side of a learning platform. The key services should include:

Personalized learning recommendations,
Interactive coding exercises
Real-time feedback to help developers improve their skills and knowledge.

Recommend the complete set of microservices and supporting server-side components I should include, along with their roles and how they should interact.
```

Prompt 3: Create the user service
```
I want to create a User Management Service for my learning platform. I will use Node.js and MongoDB. Please recommend an optimal project structure, including key folders, files, and configurations, following best practices for scalability, maintainability, and security.
```

Prompt 4: Insert code in each file with proper documentation
```
I have set up the User Management Service project using Node.js and MongoDB based on the recommended folder structure. Please give me the code that is to be included in each of the files, ensuring it follows best practices for scalability, maintainability, and security. Include all necessary fields, models, controllers, routes, middleware, and configuration files. Also include detailed documentation in each file.
```

### Test the application 

You will require a mongoDB host and password which you will add in the .env file

```
git clone https://github.com/Isi-dev/CodeCraftHub
cd CodeCraftHub
npm install
node src/app.js
```
You can prompt to generate test user data in JSOn format. e.g

```
[
  {
    "username": "john_doe",
    "email": "johndoe@example.com",
    "password": "Password123!"
  },
  {
    "username": "john_smith",
    "email": "johnsmith@example.com",
    "password": "password123!"
  }
]
```

You can now test your endpoints using Postman. For user registration, send a POST request to http://localhost:5000/api/users/register with the following request body:

```
    {
    "username": "john_smith_1",
    "email": "johnsmith_1@example.com",
    "password": "Password1234!"
    }
```

You will receive a response with status code 201 and the message "User registered successfully".

For user login, send a POST request to http://localhost:5000/api/users/login with the following request body:

```
    {
    "email": "johnsmith_1@example.com",
    "password": "Password1234!"
    }
```

You will receive a response with status code 200 and a JSON Web Token (JWT) in the response body.

### Create a Dockerfile

Prompt 5: Bundle the application in Docker
```
Can you provide the docker file to bundle the application and the MongoDB server in a container?
```

Build the docker images:
```
docker-compose build
```

Run the containers:
```
docker-compose up
```

To stop running the containers:
```
docker-compose down
```







