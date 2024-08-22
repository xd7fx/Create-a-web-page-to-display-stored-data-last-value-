# Command Control Panel

This project is a simple web application that allows users to control a device by sending commands (forward, backward, left, right, stop) to a server. The commands are stored in a database managed by phpMyAdmin and can be viewed on a confirmation page.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- You have installed PHP and MySQL on your local machine.
- You have a web server running (e.g., Apache).
- You have access to phpMyAdmin to manage your MySQL database.

## Installation

1. **Clone the repository:**

    ```bash
    git clone <repository_url>
    cd <repository_name>
    ```

2. **Set up the MySQL database:**

    - Open phpMyAdmin and create a database named `commands`.
    - Create a table named `commands` with the following structure:

    ```sql
    CREATE TABLE commands (
        id INT AUTO_INCREMENT PRIMARY KEY,
        direction VARCHAR(255) NOT NULL,
        timestamp TIMESTAMP DEFAULT CURRENT_TIMESTAMP
    );
    ```

3. **Configure the database connection:**

    - Update the database connection details in the `index.php` file:

    ```php
    $servername = "127.0.0.1:3307"; // Your MySQL server address
    $username = "root"; // Your MySQL username
    $password = ""; // Your MySQL password
    $dbname = "commands"; // Your database name
    ```

4. **Run the application:**

    - Place the project files in your web server's root directory (e.g., `htdocs` for XAMPP).
    - Open a web browser and navigate to `http://localhost/<project_folder>/index.php`.

![image](https://github.com/user-attachments/assets/fc1cb62e-c4a5-4437-aee5-f346b67ab156)


## Usage

1. **Control Panel:**

    - The control panel allows you to send commands to the server. Each button (Forward, Backward, Left, Right, Stop) will send a corresponding command.

2. **Command Confirmation:**

    - After sending a command, you will be redirected to a confirmation page displaying the last command sent.

## Project Structure

- `index.php`: The main control panel page.
- `confirmation.php`: The page displaying the last command sent.
- `README.md`: This file.

## Screenshots

### Control Panel
![Control Panel](https://github.com/user-attachments/assets/70d082a6-3ae9-48b9-b40f-9fab294a042a)

### Command Confirmation
![Command Confirmation](https://github.com/user-attachments/assets/3ede4257-d267-488f-b91b-9525784abd9c)


