# Configuration-retrieval

This project consists of a React front-end server and a Flask back-end server. The front-end server sends requests to the back-end server at various endpoints. These endpoints are /get-apt-configs, /get-snap-configs, and /get-java-configs. When requests are sent to these endpoints, the response is the output of the linux command associated with each of these endpoints. For, /get-apt-configs, the output of the command "apt list --installed" gets sent back to the front-end server after the "Get apt configs" button is clicked on. For /get-snap-configs, the output of "snap list" gets sent back after clicking the "Get snap configs" button. And for /get-java-configs, the output of "java -version" gets sent back after clicking the "Get java configs" button. It should be noted that the response for each request is in a JSON format. Each endpoint is basically a means to find out configuration information for their respective category. On top of the back-end server sending a response back to the front-end server for each request, the back-end server also stores information regarding these responses in an SQL database which is accessed through MySQL. This database consists of 3 tables where each table corresponds to the endpoint the user is sending a request to. It should be noted that the exact date and time that the responses happen is kept track of so that each record in the SQL table is unique on top of making it easier to find changes regarding the system configuration that can cause errors that prevent an application from running normally.  
