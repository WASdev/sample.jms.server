# sample.jms11
Liberty JMS 1.1 sample

This sample project contains a simple JMS Servlet application called JMSSample. JMSSample listens for HTTP requests sent to `localhost:9124/jms11-JMSSample`, and responds with various actions.
There are 2 main Servlets that are contained:

1. P2P : Point-to-Point Messaging uses JMS Queue to send and receive messages.  It also contains MDB message send and response.

2. PubSub : Publish-and-Subscribe Messaging uses JMS topic to send and receive messages. 

## Running with Maven

This project can be build with [Apache Maven](http://maven.apache.org/). The project uses [Liberty Maven Plug-in][] to automatically download and install Liberty profile runtime from the [Liberty repository](https://developer.ibm.com/wasdev/downloads/). Liberty Maven Plug-in is also used to create, configure, and run the application on the Liberty server. 

Use the following steps to run the application with Maven:

1. Set the `IBM_LIBERTY_LICENSE` environment property with the license code found in the Liberty license file. See the following [instructions][Liberty License Instructions] on obtaining the license code. 
    ```bash
    $ export IBM_LIBERTY_LICENSE=<license code>
    ```

2. Execute full Maven build. This will cause Liberty Maven Plug-in to download and install Liberty profile server.
    ```bash
    $ mvn -Pwlp clean install
    ```

Once the server is running, the Queue application actions will be available under :

[http://localhost:9124/jms11-JMSSample/JMSSampleP2P?ACTION=listAction](http://localhost:9124/jms11-JMSSample/JMSSampleP2P?ACTION=listAction).

the Topic application actions will be available under :

[http://localhost:9124/jms11-JMSSample/JMSSamplePubSub?ACTION=listAction](http://localhost:9124/jms11-JMSSample/JMSSamplePubSub?ACTION=listAction).

3. To stop the Liberty server, execute the following (Note: If you would like to re-install Liberty, first you must stop the Liberty sserver with this command, otherwise installation will fail:
    ```bash
    $ mvn liberty:stop-server
    ```

4. To start the Liberty server, execute the following:
    ```bash
    $ mvn liberty:start
    ```

	
# Notice

© Copyright IBM Corporation 2015.

# License

```text
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
````

[Liberty Maven Plug-in]: https://github.com/WASdev/ci.maven
[Liberty License Instructions]: https://github.com/WASdev/ci.maven#using-a-repository

