# Minimal Postgres Example #
This repository makes use of Docker to create a PostgreSQL sandbox.

Start the server in the container:
    docker-compose up

In another shell, run the client in the container:
    docker exec -it demo-postgres psql -U postgres

Create an example table:
    CREATE TABLE states (
        names text,
        abbreviation text
    );

Load example data:
    COPY states FROM '/postgres/host/states.csv' WITH CSV HEADER;

## License notice ##

This work is released under
[CC0](https://creativecommons.org/publicdomain/zero/1.0/).
See LICENSE for more details.

The person who associated a work with this deed has dedicated the work to the
public domain by waiving all of his or her rights to the work worldwide under
copyright law, including all related and neighboring rights, to the extent
allowed by law.
