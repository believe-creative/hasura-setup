# Hasura-setup
* Hasura only works with PostgreSql
## Running hasura locally with fresh postgreSQL.
* Install virtalbox and vagrant locally https://www.virtualbox.org/wiki/Download_Old_Builds_5_2  and https://www.vagrantup.com/downloads.html
* Clone the repo into a directory
* Run the following command
``` vagrant up ```
* After command completion,goto browser http://127.0.0.1:8081 for hasura
## To use existing postgre database
* Edit param HASURA_GRAPHQL_DATABASE_URL in docker-compose.yml. 
> Usual database string format postgres://[user]:[password]@[host]:5432/[database]
## If docker already installed in the machine and want to run one liner
``` docker run -d -p 8080:8080 -e HASURA_GRAPHQL_DATABASE_URL=postgres://username:password@hostname:port/dbname -e HASURA_GRAPHQL_ENABLE_CONSOLE=true hasura/graphql-engine:latest ```
