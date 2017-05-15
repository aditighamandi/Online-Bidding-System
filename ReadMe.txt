How to run:

1. Install Node.js and make sure that "node" command works on command line or terminal
2. Install MongoDB and run "mongod" command to start the mongoDB server
3. Create a keystore and remember the password
4. Install Apache Tomcat and make changes in the server.xml to run with 
   SSL/TLS and enable compresison by adding the following line
  
   <Connector
           protocol="org.apache.coyote.http11.Http11NioProtocol"
           port="8443" maxThreads="200"
           scheme="https" secure="true" SSLEnabled="true"
           keystoreFile="KEYSTORE_PATH" keystorePass="KEYSTORE_PASSWORD"
           clientAuth="false" sslProtocol="TLS"
	   compression="on" 
	   compressionMinSize="0" 
	   noCompressionUserAgents="gozilla, traviata" 
	   compressableMimeType="text/html,text/css,application/json,application/javascript"/>

5. Copy the "Client" folder to Webapps folder of Apache Tomcat
6. Start the Apache Tomcat Server
7. Open Command line and go to "Server" folder
8. Start the server by using the command "node server.js"
9. Open chrome and go to https://localhost:8443/Client to start the application