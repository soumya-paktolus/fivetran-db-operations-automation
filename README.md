# Fivetran Local Data Processing Test Automation

## Overview

This repository contains a test automation framework for Fivetran Local Data Processing, including scripts to create a PostgreSQL database, perform DML and DDL operations, and validate the results. The automation scripts are integrated into the CI pipeline using GitHub Actions.

## Table of Contents

- Project Structure
- Setup Instructions
- Test Execution
- CI Pipeline
- Contributing


## Project Structure

The project is organized into the following directories:

- `src`: Contains Python scripts for database operations (`db_operations.py`), main setup logic (`main.py`), and constants (`constants.py`).
- `test`: Includes test scripts for database connection (`test_db_connection.py`) and DDL/DML operations (`test_ddl_dml_operations.py`).
- `database.sql`: SQL script to create the operations database and tables.
- `pyproject.toml`: Configuration file for build system and pytest.
- `pytest.ini`: Configuration file for pytest.
- `requirements.txt`: List of dependencies.
- `setup.cfg`: Configuration file for project options.
- `README.md`: Project documentation.

## Setup Instructions

1. Clone the repository:

   ```bash
   git clone https://github.com/your_username/fivetran-local-data-processing.git
   ```

2. cd into the directory:

   ```bash
   cd databaseOperations-main
   ```

3. Add your username and some random password in place of "username" and "password" in config.ini to connect to your local database

   ```bash
   user = <your_username>
   password = <your_password>
   ```

4. Download all the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

## Test Execution

Run the tests using pytest:

```bash
pytest
```
<img width="1306" alt="image" src="https://github.com/soumya-paktolus/db-automation-pipeline/assets/157735406/bc823b33-ec98-464c-ba70-89861b4613c5">


## CI Pipeline

The project is configured with GitHub Actions for continuous integration. The pipeline includes steps to install dependencies, set up PostgreSQL, and execute tests.

The CI workflow is triggered on every push to the main branch.

