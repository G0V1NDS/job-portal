## Job Portal

This repo holds the code for the Job Portal server backend.

### Initial setup

- Clone the repo and `cd` into it
`git clone https://github.com/G0V1NDS/job-portal.git && cd job-portal;`

- Create the virtualenv
`python3 -m venv env`

- Activate the virtualenv
`source env/bin/activate`

- Install the requirements
`pip install -r requirements.pip`

### Setting up environment variables

- Create a file named `.env` in project root, refer `.env.example`

- Create database in local mysql, it should have the same name which is defined as `DB_NAME` in .env file
`create database <DB_NAME>`  # Run in mysql client

- Use below command to export the variables defined in `.env`
`set -a; source .env; set +a;`

### Setting up Database

- Run migrations to generate db tables
`python manage.py migrate`

- Creating `admin` user
`python manage.py createsuperuser --email admin@example.com --username admin`


### Running the server

`./manage.py runserver`
