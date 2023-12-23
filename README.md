# Configuration-retrieval

This project consists of a React front-end server and a Flask back-end server. The front-end server sends a request to the back-end server at any of the three endpoints. There are three buttons on the front-end server that dictate which endpoint a request gets sent to. When a request is sent after clicking a button, the response is the configuration information in JSON pertaining to the endpoint chosen. This configuration information is generated from the output of a Linux command specific to the chosen endpoint. When a response is sent from the back-end server to the front-end server, the back-end server works to store that response in an SQL database. This database is accessed through MySQL and consists of three tables that correspond to each endpoint. The exact date and time a response gets generated is kept track of so that each record in the SQL table is unique on top of making it easier to find changes regarding the system configuration that can cause errors that prevent an application from running normally.
