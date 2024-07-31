# Installation and Setup Instructions

## Installing NVM

1. Follow the instructions to install NVM [here](https://github.com/nvm-sh/nvm).
2. Install and use Node.js 14:

    ```bash
    nvm install 14
    nvm use 14
    ```

## Cloning the Repository and Switching Branch

1. Clone the repository:

    ```bash
    git clone https://github.com/marcogarofal/AndronEconomy.git
    ```

2. Switch to the branch:

    ```bash
    git checkout abbonamenti
    ```

## Installing and Configuring MySQL

1. Install MySQL:

    ```bash
    sudo apt-get install mysql-server
    ```

2. Configure the database:

    ```bash
    cd Altro/
    sudo mysql -u root
    ```

    In the MySQL console, execute:

    ```sql
    CREATE DATABASE Andron;
    USE Andron;
    EXIT;
    ```

3. Import the SQL dump:

    ```bash
    sudo mysql -u root Andron < dump_3.sql
    ```

4. Configure the MySQL user:

    ```bash
    sudo mysql -u root
    ```

    In the MySQL console, execute:

    ```sql
    ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'provaPass';
    ```

## Installing Dependencies and Starting the Python Server

1. Navigate to the Python server directory:

    ```bash
    cd ../Server_python/Server/
    ```

2. Install the required libraries:

    ```bash
    pip3 install Flask==2.1.3
    pip3 install Werkzeug==2.2.2
    pip3 install flask_jwt_extended
    pip3 install flask_cors
    pip3 install pymysql
    pip3 install python-dateutil
    pip3 install requests
    ```

3. Start the Python server:

    ```bash
    python3 server.py
    ```

## Starting the App

1. Navigate to the app directory and update the IP addresses:

    ```bash
    cd ../../App/
    ```

2. Start the app:

    ```bash
    npm start
    ```

## Starting the Administration

1. Navigate to the administration directory and start it:

    ```bash
    cd ../Amministrazione/
    npm start
    ```
