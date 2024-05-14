# Fyle Backend Challenge




## Installation

1. Fork this repository to your github account
2. Clone the forked repository and proceed with steps mentioned below

### Install requirements

```
virtualenv env --python=python3.8
source env/bin/activate
pip install -r requirements.txt
```
### Reset DB

```
export FLASK_APP=core/server.py
rm core/store.sqlite3
flask db upgrade -d core/migrations/
```

### Run Tests 

```
bash single_run.sh
```

### Start Server

```
bash run.sh
```

### Build the Docker image:
`docker build -t flask-app .`

### Run the Docker container:
`docker run -p 7755:7755 flask-app`

It will be accessible at http://localhost:7755 


## Building and Running with Docker Compose


### Run the Docker Compose command: 
`docker-compose up` 

This will build the Docker image, accessible at `http://localhost:7755`.

### To stop the Docker Compose services, press Ctrl + C, and then run:
`docker-compose down` 

This will stop and remove the containers, networks, and volumes.



