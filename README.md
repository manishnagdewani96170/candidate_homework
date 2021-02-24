# Candidate Homework

## Getting started

* Install Postgres
* Ensure there is a user called `candidate_homework` with an empty password, or update the username and password in `config/database.yml`
* run `rake db:setup`
* run `rake db:seed`

## Prompt 1 - Data model changes and migration

You'll find an Integration model that holds connections in it's `config` jsonb column. We'll say this model grew organically and required multiple connections to be in a single integration record. Now we need to split it up. We need to get individual records for items in the `field_mappings` portion of a connection, while maintaining it's connection to the `path` information.

1. Add additional models where needed.
2. Write database migrations to add the new table or tables.
3. Write a script that can take the data added to the db through the database seed and put it into the new data model you design.

### Evaluation

To evaluate, we will run the same steps as the "Getting started" section above, and then apply your changes. After your changes are applied we will run the new database migration(s) and your script for data migration.
