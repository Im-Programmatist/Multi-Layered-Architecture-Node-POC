# Multi-Layered-Architecture-Node-POC

<code>
  <pre>
  project-root/
    ├── src/
    │   ├── controllers/
    │   │   └── UserController.js
    │   │
    │   ├── middlewares/
    │   │   └── jwt_middleware.js
    │   │
    │   ├── daos/
    │   │   └── UserDao.js
    │   │
    │   ├── models/
    │   │   └── User.js
    │   │
    │   ├── routes/
    │   │   └── userRoutes.js
    │   │
    │   ├── services/
    │   │   └── UserService.js
    │   │
    │   ├── validators/
    │   │   └── userValidator.js
    │   │
    |   ├── constant/
    │   │   └── .env
    │   |   └── const_message.js/json
    │   │
    |   ├── Utils(Helper)
    │   │   └── any helper file.js
    │   │
    │   └── app.js
    │
    ├── config/
    │   ├── database_config.js
    │   ├── config_other.js
    │   ├── logger_config.js
    │   └── ...
    │
    ├── logs/
    │   ├── application.log
    │   ├── ...
    │
    ├── migrations/
    │   ├── ...
    │
    ├── Logger/
    │   ├── logger.json
    │   ├── logger.js
    │
    ├── public/
    │   ├── HTML
    |   ├── Swagger
    │
    ├── test/
    │   ├── ...
    │
    ├── docker
    │
    ├── .sequelizerc
    │
    ├── .gitignore
    │  
    ├── jenkins
    │
    └── index.js
  </pre>
</code>

## Here's a breakdown of each component:

Controllers: Handle incoming requests, validate inputs, and interact with services. They are responsible for managing the HTTP layer.

DAOs (Data Access Objects): Interact with the database. Abstract the database-related operations and queries.

Models: Define Sequelize models that represent your database tables and relationships.

Routes: Define Express routes and connect them to controllers. Handle routing logic.

Services: Contain the core business logic of your application. Coordinate interactions between controllers and DAOs.

Validators: Handle input validation and data sanitization. Ensure that input data is valid before proceeding to business logic.

Config: Store configuration settings, such as database connection details, API keys, etc.

Migrations: Store database migration scripts for managing schema changes over time.

Logging: Configure and manage logging for your application. This could be a separate component or handled within the config folder.

index.js: The entry point of your application, where you set up and start the server.


## When & Where to use Configuration ("config") & ENV File

Configuration ("config"): 
  1. Configuration refers to settings and parameters that control the behavior of your application. 
  2. Can mention things like database connection strings, API keys, feature toggles, and more.
  3. You want to have different database connection settings for development and production environments.

Environment Variables ("env"):
  1. Environment variables are dynamic values that are external to your application and can affect its behavior. 
  2. Environment variables are particularly useful for sensitive data (like API keys and passwords) that you don't want to hardcode in your codebase.
  3. Suppose your application relies on an external API and requires an API key to access it. Instead of hardcoding the API key in your code, you can use an environment variable
  4. To set environment variables, you can do so directly in your operating system's environment or by using tools like .env files (with libraries like dotenv) during development. 


## Reference 
https://thekenyandev.com/blog/routes-controllers-services-and-models-daos-in-a-nodejs-api-layered-architecture-in-depth/
