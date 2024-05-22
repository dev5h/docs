# Installing LAMPP Stack

## Update Packages
```bash
sudo apt update
```

## Install and enable Apache

```bash
sudo apt install apache2
sudo systemctl start apache2
sudo systemctl enable apache2
```

## Install MySQL 

```bash
sudo apt install mysql-server
```
### Configure MySQL
Run `sudo mysql_secure_installation`

And secure mysql installation. After tht login to your root shell

```bash
sudo mysql -u root
```

**Change The Default Password**

Execute these MySQL commands one by one

1. **Switch to the `mysql` database**:

    ```sql
    USE mysql;
    ```

2. **Change the authentication method to `mysql_native_password` and set a password**:

    ```sql
    ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'your_new_password';
    ```

3. **Flush the privileges** to ensure the changes take effect:

    ```sql
    FLUSH PRIVILEGES;
    ```

4. **Exit MySQL**:

    ```sql
    EXIT;
```

## Install PHP

```bash
sudo apt install php libapache2-mod-php php-mysql
```

## Installation phpMyAdmin

```bash
sudo apt install phpmyadmin
```


### Wrap Up
Finally run ```sudo systemctl restart apache2```


And it should be installed
