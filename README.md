<div style="display: inline">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d9/Node.js_logo.svg/220px-Node.js_logo.svg.png" width="auto" height="64px">
  <img src="https://expressjs.com/images/express-facebook-share.png" width="auto" height="64px">
</div>


This project is based on [express-sequelize-boilerplate](https://github.com/gadfaria/express-sequelize-boilerplate) : A boilerplate for express.js with integration for Sequelize and Postgres.

## Getting Started 

```bash
# Clone the repository
git clone https://github.com/gadfaria/express-sequelize-boilerplate.git

# Enter into the directory
cd express-sequelize-boilerplate/

# Install the dependencies
yarn

# Set the environment variables:
cp .env.example .env

# If database exists, run migrations:
yarn sequelize db:migrate 

# Running the boilerplate:
yarn dev
```

## Configuration

> NOTE: At this time in the project, JWT and AWS support has been commented out, but left in place for reference.

Variables for the environment

| Option | Description |
| ------ | ------ |
| SERVER_PORT | Port the server will run on |
| SERVER_JWT | true or false |
| SERVER_JWT_SECRET | JWT secret |
| SERVER_JWT_TIMEOUT | JWT duration time |
| DB_DIALECT | "mysql", "postgresql", among others |
| DB_HOST | Database host |
| DB_USER | Database username |
| DB_PASS | Database password |
| DB_NAME | Database name |
| AWS_KEYID | Access key ID |
| AWS_SECRETKEY | User secret key |
| AWS_BUCKET | Bucket name |


## Commands for sequelize 
```bash
# Creates the database
yarn sequelize db:create 

# Drops the database
yarn sequelize db:drop 

# Load migrations
yarn sequelize db:migrate 

# Undo migrations
yarn sequelize db:migrate:undo:all 

# Load seeders (Note, there is no seeders code written at this time)
yarn sequelize db:seed:all
```

## Building out the application

This boilerplate takes a more 'enterprisey' approach to handling its tables and resources. To add models properly within this context requires writing migrations as found in `src/database/migrations`. Of course, models, controllers and routes for each resource will have to be placed in each of the respective folders: 

- `src/controllers`
- `src/models`
- `src/routes`

