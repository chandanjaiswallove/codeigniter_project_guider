# CodeIgniter Project Guide & Help

## Before Starting Your Project

First, set up your Web Server / Local Development Server. After completing the server setup, proceed with the CodeIgniter Framework setup.

---

# 🖥️ Web Server Setup

| Operating System | Web Server Package | Components           | Download / Install Source                               |
| ---------------- | ------------------ | -------------------- | ------------------------------------------------------- |
| Windows          | XAMPP              | Apache + PHP + MySQL | Official Website: https://www.apachefriends.org         |
| Windows          | WAMP               | Apache + PHP + MySQL | Official Website: https://wampserver.com/en/            |
| Ubuntu (Linux)   | LAMP Stack         | Apache + PHP + MySQL | Install using Ubuntu terminal commands and repositories |

---

# Install VS Code

Before starting development, download and install Visual Studio Code (VS Code).

Open VS Code and open your project folder.

---

# CodeIgniter 3 Initial Project Setup

### Step 1: Download CodeIgniter 3

Download CodeIgniter 3 and rename the extracted folder to your project name.

Example:

ProjectName

---

### Step 2: Create .htaccess File

Create a new file named `.htaccess` inside the project root folder and add the following code:

```apache
RewriteEngine On

RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d

RewriteRule ^(.*)$ index.php/$1 [L]
```

---

### Step 3: Configure index.php

Open `index.php` and modify the development environment settings:

```php
case 'development':
    error_reporting(-1);
    ini_set('display_errors', 0);
break;
```

---

### Step 4: Configure Autoload

File Path:

```text
application/config/autoload.php
```

Update libraries and helpers:

```php
$autoload['libraries'] = array(
    'database',
    'email',
    'session'
);

$autoload['helper'] = array(
    'html',
    'form',
    'file',
    'url',
    'text',
    'string'
);
```

---

### Step 5: Configure Base URL

File Path:

```text
application/config/config.php
```

Update:

```php
$config['base_url'] = 'http://localhost/ProjectName/';
$config['index_page'] = '';

$config['composer_autoload'] = 'vendor/autoload.php';
```

---

### Step 6: Configure Database

File Path:

```text
application/config/database.php
```

Update database credentials:

```php
'hostname' => 'localhost',
'username' => 'root',
'password' => 'Admin1234#@',
'database' => 'DB_Name',
'dbdriver' => 'mysqli',
```

---

# Connect Project with Git & GitHub

After completing the CodeIgniter configuration:

### Initialize Git

```bash
git init
```

### Add Files

```bash
git add .
```

### Commit Changes

```bash
git commit -m "Initial Project Setup"
```

### Connect GitHub Repository

```bash
git remote add origin https://github.com/username/repository.git
```

### Push Project

```bash
git branch -M main

git push -u origin main
```

---

# Start Project Development

After completing:

✅ Web Server Setup

✅ CodeIgniter Configuration

✅ Database Configuration

✅ Git & GitHub Integration

You can start developing your project.

---

# Follow MVC Architecture

CodeIgniter follows the MVC (Model View Controller) pattern:

### Model

* Database Operations
* Insert, Update, Delete, Select Queries

### View

* HTML Pages
* UI Design
* Forms
* User Interface

### Controller

* Business Logic
* Request Handling
* Data Processing
* Calling Models and Views

---

# Basic Project Structure

```text
application/
│
├── controllers/
│   ├── Dashboard.php
│   ├── Login.php
│
├── models/
│   ├── DashboardModel.php
│   ├── LoginModel.php
│
├── views/
│   ├── dashboard.php
│   ├── login.php
│
├── config/
│
└── helpers/
```

---

# Initial Development Work

Start with:

* Routing Setup
* Controllers Creation
* Models Creation
* Views Creation
* Authentication Module
* Dashboard
* CRUD Operations
* Database Design
* Form Validation
* Session Management
* Email Configuration

---

# Project Workflow

1. Setup Server
2. Download CodeIgniter
3. Configure Project
4. Connect Database
5. Setup Git & GitHub
6. Follow MVC Structure
7. Create Modules
8. Develop Features
9. Test Application
10. Deploy Project

This is the standard process to start a CodeIgniter 3 project from scratch and maintain a proper MVC-based development workflow.
