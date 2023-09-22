# Using Datastax Astra Vector Database with Bedrock

The quickstart is designed to run out-of-the-box as a notebook in
Google Colaboratory ("Colab" for short)
using Astra DB as the Vector Database.

## Vector Database

Create your Vector Database with Astra DB: it's free, quick and easy.

??? info "What is Astra DB?"

    Astra DB is a serverless DBaaS by DataStax, built on Apache Cassandra. It offers
    a free tier with generous traffic and storage limits. Using Astra DB frees you
    from the hassle of running your own cluster while retaining all the advantages, such as the excellent data distribution and very high availability that make Cassandra a world-class NoSQL database.

### Create the Database

Go to [astra.datastax.com](https://astra.datastax.com) and sign up.

Click "Create Database" and _make sure to select_ "Serverless with Vector Search".

In the following we assume you called the database `cassio_db`.
You will also be asked for a "Keyspace name" when creating the database:
you can call it something like `cassio_tutorials` for example.
(A keyspace is simply a way to keep related tables grouped together.)

In a couple of minutes your database will be in the "Active" state, as
shown in the DB Quickstart page.

Detailed explanations can be found
[at this page](https://awesome-astra.github.io/docs/pages/astra/create-instance/).

### Database Access Token

Now you need credentials to connect securely to your database.

On the DB Connect panel, locate the "Create a custom token" link
and generate a new token **with role "Database Administrator"**. _Make sure you
safely store all parts of the Token: it will not be shown
anymore for security reasons._

Detailed information on DB Tokens can be found
[here](https://awesome-astra.github.io/docs/pages/astra/create-token/).

### Database Secure Connect Bundle

Next, you need a "Secure Connect Bundle" zipfile, containing certificates
and routing information for the drivers to properly establish a connection to
your database.

On the DB Connect panel, find the "Get Bundle" button and click on it.
You don't need to unpack the zip file, just save it on you computer: you
will need it momentarily.

For more info on the Secure Connect Bundle
see [this page](https://awesome-astra.github.io/docs/pages/astra/download-scb/#c-procedure).

## LLM Access

In order to run the quickstart, you will need to get access to AWS Bedrock and retrieve
temporary credentials for the code to use.

## Run the quickstart

Once you have the Token and the Secure Connect Bundle,
and the secrets required to use an LLM, click on the Colab Notebook link below
to start using your Vector Search Database in the LangChain QA example:

<p align="center">
  <a href="http://colab.research.google.com/github/CassioML/cassio-website/blob/main/docs/frameworks/langchain/.colab/colab_qa-basic.ipynb" target="blank;">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" style="height: 2.0em; vertical-align: middle;"/>
  </a>
</p>
