# Cascada API

This is a Python API that serves the **[Cascada](http://project-cascada.herokuapp.com/)** website. The reposity for the website is located [here](https://github.com/phelanjo/cascada-server)

## How It Works
* Using SQLAlchemy and Flask, a Python web application is instantiated and a table named "Waterfall" is created. It is then connected to an AWS RDS PostgreSQL database instance.

* Waterfall table schema:
  * **id**: Unique waterfall ID. Serves as the primary key in the table.
  * **name**: Name of waterfall.
  * **height**: Vertical length (height) of waterfall.
  * **latitude**: Latitude coordinate of waterfall.
  * **longitude**: Longitude coordinate of waterfall
  
* Endpoints:
  * /fetch_all/ - Returns a list of waterfalls from the database to be consumed by the front-end.
  * /fetch_waterfall_by_name/ - Returns a single waterfall's unique ID from the database given its name.
  * /add_waterfall/ - Adds a waterfall to the database.
  * /edit_waterfall/ - Edits an existing waterfall in the database.
  * /delete_waterfall/ - Deletes a waterfall from the database.

*__Please Note -- It is not possible to run this API locally without your own RDS PostgreSQL database instance.__*

## Dependencies
The **Cascada** API utilizes a few Python dependencies, which include:
* [Flask](https://pypi.org/project/Flask/): A web framework that helps build web applications in Python.  
`pip install -U Flask`  

* [Flask-SQLAlchemy](https://pypi.org/project/Flask-SQLAlchemy/): A Flask extension that adds support for SQLAlchemy.  
`pip install Flask-SQLAlchemy`  

* [SQLAlchemy](https://pypi.org/project/SQLAlchemy/): A Python Object Relational Mapper (ORM) that makes writing SQL statements easier.  
`pip install SQLAlchemy`  

* [psycopg2](https://pypi.org/project/psycopg2/): A PostgreSQL adapter that helps in connecting to the database.  
`pip install psycopg2`  

* [python-dotenv](https://pypi.org/project/python-dotenv/): Allows the usage of a `.env` file to hide sensitive credentials.  
`pip install python-dotenv`  
