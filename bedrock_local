The easiest way to work with the quick start is to use the coLab
environment, but if you wish to work with the notebooks locally,
here is some information for you to use.

## Run with local Jupyter

There are several reasons one might prefer to launch the code locally:
for example, it may be easier to evolve the notebooks
into a full-fledged application; also, one can prefer a non-ephemeral
setup, especially when planning to run several examples in a row.

In the following we assume you have fulfilled the
[pre-requisites](/bedrock_setup/#vector-database) listed on the previous page.

You should have basic familiarity with `git` and the shell console.

### Clone this repository

First, clone this repo on you machine
(it spans both the website and the examples).
In a directory of your choice, execute the following:

```
git clone https://github.com/synedra/astra_vector_examples
cd notebooks
```

Note that the following commands are to be run in the `notebook` directory.

### DB

You need a `.env` file which defines the database credentials and connection
parameters.

You can copy the provided `.env.template` file and replace
the environment variables you see there
(essentially, the full path to the bundle file, the keyspace
name and your database secret token string).

??? tip "Using the Astra CLI"

    Alternatively, once you have the Database Administrator token,
    you can use the Astra CLI to automate the rest (secure-connect bundle and `.env` file).

    First [install Astra CLI](https://awesome-astra.github.io/docs/pages/astra/astra-cli/#1-installation).

    Then configure it with:

    ```
    astra setup
    ```

    providing the Database Administrator token you created earlier
    (the string starting with `AstraCS:...`).

    Finally, in the root directory of this repo, adjusting names if needed, launch

    ```
    astra db create-dotenv vector -k vector
    ```

    This will download the bundle zipfile and create a `.env` file
    with all connection parameters you'll need later.

### Bedrock Credentials

In this repo's root directory again, create a `.api_keys` file where the secrets
necessary for Bedrock are defined. You can copy
the provided `.api_keys.template` and adjust the values therein.

Remember to "source" this file before launching notebooks or Python scripts:

```
. .api_keys
```

the `localSession` object will then be passed exactly in the same way
as you would a connection to Astra DB
(see [the drivers documentation](https://docs.datastax.com/en/developer/python-driver/latest/getting_started/#connecting-to-cassandra) for more options).
