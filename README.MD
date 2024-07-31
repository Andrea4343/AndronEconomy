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
    cd Altro/DUMP\ DB/DUMP/
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
    sudo mysql -u root Andron < dump.sql
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

1. Navigate to the Python server directory and install dependencies:

    ```bash
    cd Server_python/
    pip3 install -r requirements.txt
    ```

2. Install the required libraries:

    ```bash
    cd Server/
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

    Replace all IP addresses `192.168.1.53` or `51.68.190.11` with `127.0.0.1`.

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

    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
# Istruzioni per l'installazione e configurazione

## Installazione di NVM

1. Segui le istruzioni per installare NVM [qui](https://github.com/nvm-sh/nvm).
2. Installa e usa Node.js 14:

    ```bash
    nvm install 14
    nvm use 14
    ```

## Clonazione del Repository e Cambio del Branch

1. Clona il repository:

    ```bash
    git clone https://github.com/marcogarofal/AndronEconomy.git
    ```

2. Cambia il branch:

    ```bash
    git checkout abbonamenti
    ```

## Installazione e Configurazione di MySQL

1. Installa MySQL:

    ```bash
    sudo apt-get install mysql-server
    ```

2. Configura il database:

    ```bash
    cd Altro/DUMP\ DB/DUMP/
    sudo mysql -u root
    ```

    All'interno della console MySQL, esegui:

    ```sql
    CREATE DATABASE Andron;
    USE Andron;
    EXIT;
    ```

3. Importa il dump SQL:

    ```bash
    sudo mysql -u root Andron < dump.sql
    ```

4. Configura l'utente MySQL:

    ```bash
    sudo mysql -u root
    ```

    All'interno della console MySQL, esegui:

    ```sql
    ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'provaPass';
    ```

## Installazione delle Dipendenze e Avvio del Server Python

1. Vai nella directory del server Python e installa le dipendenze:

    ```bash
    cd Server_python/
    pip3 install -r requirements.txt
    ```

2. Installa le librerie necessarie:

    ```bash
    cd Server/
    pip3 install Flask==2.1.3
    pip3 install Werkzeug==2.2.2
    pip3 install flask_jwt_extended
    pip3 install flask_cors
    pip3 install pymysql
    pip3 install python-dateutil
    pip3 install requests
    ```

3. Avvia il server Python:

    ```bash
    python3 server.py
    ```

## Avvio dell'App

1. Vai nella directory dell'app e modifica gli IP:

    ```bash
    cd ../../App/
    ```

    Modifica tutti gli IP `192.168.1.53` o `51.68.190.11` con `127.0.0.1`.

2. Avvia l'app:

    ```bash
    npm start
    ```

## Avvio dell'Amministrazione

1. Vai nella directory dell'amministrazione e avvia:

    ```bash
    cd ../Amministrazione/
    npm start
    ```
