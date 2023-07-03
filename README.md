This is a base node.js project template, which anyone can use as it has been prepared by keeping in mind some of the most important code principles and project management recommendations. Feel free to change anything.

 `src` -> Inside the src folder all the actual source code regarding the project will reside. This will not include any kind of tests. (You might want to make a separate `tests` folder).

Let us take a look inside the `src` folder :-

- `config` -> In this folder anything and everything regarding any configurations of setup of a library or module will be done. For example, setting up `dotenv` so that we can use the environment variables in a cleaner fashion, this is done inside the `server-config.js` file. One more example can be setting up of the logging library aht can help you prepare meaningful logs, so configuration for this library can be done here. 

- `routes` -> In this folder we register the route and the corresponding middlewares and routes for it.

- `middlewares` -> They are going to inctercept the incoming requests where we write our validators, authenticatos etc.

- `controllers` -> They are kind of the last middlewares as post them you call your business layer to execute the business logic. In controllers, we just receive the incoming requests and data and pass it on to the business layer, and once business layer returns an output we structure the the API response in the controller and send the output. 

- `repository` -> This folder contains all the logic using which we interact with the DB y writing queries, all the raw queries or ORM queries will go here. 

- `services` -> Contains the business logic and interacts with the repositories for the data from the DB.

- `utils` -> Contains helper functions.

### Setting up the project :-

- Download this template from github and open it in your preferred editor.
- In the root directory, create a `.env` file and add the following environment variables
    ``` 
        PORT=<port number of your choice>
    ```
    eg:
    ```
        PORT=3000
    ```

- Inside the `src/config` folder, create a file named as config.json and write the following code:
    ```
        {
            "development": {
                "username": "root",
                "password": null,
                "database": "database_development",
                "host": "127.0.0.1",
                "dialect": "mysql"
            },
            "test": {
                "username": "root",
                "password": null,
                "database": "database_test",
                "host": "127.0.0.1",
                "dialect": "mysql"
            },
            "production": {
                "username": "root",
                "password": null,
                "database": "database_production",
                "host": "127.0.0.1",
                "dialect": "mysql"
            }
        }
    ```

- If you are setting up your development environment, then write the username of your DB, password of your DB, and in dialect mention whatever DB you are using ( Eg:- MySQL, MariaDB etc.).




