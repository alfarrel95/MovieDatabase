# Movie Database

## How to setup locally

### Install dependencies

```shell
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### Create the Neo4j database with correct data

Go to [Neo4j's Sandbox](https://sandbox.neo4j.com/) and create a new project, select Movies under Pre Built Data. Go to `Connection details` and grab your credentials to add it to the following environment variable:

```shell
export NEO4J_BOLT_URL=bolt://neo4j:password@host-or-ip:port
```

Run migrations and create your superuser (for the admin, this is using an SQLite database)

```
./manage.py migrate
./manage.py createsuperuser
```

### Run the server

```shell
python manage.py runserver
```

Now you should be able to access http://localhost:8000 and play with the app.

