FROM python:3.9.19-slim


## Environment Variables
ENV APP_PORT=5153
ENV DB_USERNAME=USERNAME
ENV DB_PASSWORD=PASSWORD
ENV DB_HOST=127.0.0.1
ENV DB_PORT=5432
ENV DB_NAME=postgres

## Create app directory
WORKDIR /app

# Update the local package index with the latest packages from the repositories
RUN apt update -y

# Install a couple of packages to successfully install postgresql server locally
RUN apt install build-essential libpq-dev -y

# Update python modules to successfully build the required modules
RUN pip install --upgrade pip setuptools wheel

# Install app dependencies
COPY analytics/requirements.txt ./

RUN pip install -r requirements.txt

# Bundle app source
COPY analytics /app

EXPOSE 5153
CMD [ "python", "app.py" ]