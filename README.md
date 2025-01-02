# Simple Login Simulation with PHP and MySQL

Hello there! I'm thrilled to share this very basic login simulation project with you. It's a simple example of how to create a login form using HTML, process it with PHP, and interact with a MySQL database.  I made this with the hope that it might be helpful to someone just starting out with web development, or perhaps as a quick refresher for others.

It is not intended for production use, but rather as an educational tool.

## What's Inside?

This repository contains a single PHP file (`login.php`) that handles both the display of an HTML login form and the server-side processing of login requests.  It's designed to be straightforward and easy to follow.

## How to Use It (Step-by-Step Guide)

I've tried my best to make the setup as painless as possible. Here's how you can get this little project up and running:

1.  **Prepare Your Database:**

    First, you'll need a MySQL database.  Please run the following SQL commands to create a test database and a user table:

    ```sql
    CREATE DATABASE test_db;
    USE test_db;

    CREATE TABLE users (
        id INT AUTO_INCREMENT PRIMARY KEY,
        username VARCHAR(50) NOT NULL,
        password VARCHAR(255) NOT NULL
    );

    INSERT INTO users (username, password) VALUES ('testuser', 'testpassword');
    ```

    This will create a database named `test_db` with a `users` table, and add a sample user you can test with.

2.  **Update Database Credentials:**

    In the `login.php` file, you'll need to change the database credentials to match your setup. Look for this line:

    ```php
    $connection = new mysqli('localhost', 'your_db_user', 'your_db_password', 'your_db_name');
    ```
    Replace `'localhost'`, `'your_db_user'`, `'your_db_password'`, and `'your_db_name'` with your actual database host, username, password, and the database name (`test_db` if you used the SQL above).
    You may update that line with this:
    ```php
    $connection = new mysqli('localhost', 'root', 'your password', 'test_db');
    ```
    And replace `'your password'` with your actual password.

3.  **Start a Local Server:**

    The easiest way to run this is using PHP's built-in server. Open your terminal or command prompt, navigate to the directory where you saved `login.php`, and run:

    ```bash
    php -S localhost:8000
    ```

    This will start a server on port 8000.

4.  **Open in Your Browser:**

    Now, open your favorite web browser and go to:

    ```
    http://localhost:8000/login.php
    ```

    You should see the login form!

5.  **Test it Out:**

    Try logging in with the username `testuser` and password `testpassword`. If all goes well, you'll see a success message. You can also try entering incorrect credentials to see what happens.

## A Few Notes

*   This is a simplified example for learning purposes. It does not include many security features that would be essential in a real-world application (like password hashing).
*   I'm always open to suggestions and feedback on how to make this project better. If you spot any issues or have ideas for improvements, please feel free to open an issue or submit a pull request.

## Acknowledgements

I would like to express my gratitude to the developers of PHP and MySQL. The ease of use of these technologies allowed me to quickly create a project that I hope will help others on their learning journey in web development.

## Thank You!

Thanks for checking out this little project. I hope you find it useful in some small way!  Happy coding!
