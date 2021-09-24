# sample.jms.server

Liberty JMS sample

This sample project contains a simple JMS Servlet application called JMSSample. JMSSample listens for HTTP requests sent to `localhost:9124/jms11-JMSSample`, and responds with various actions.
There are 2 main Servlets that are contained:

1. P2P : Point-to-Point Messaging uses JMS Queue to send and receive messages.  It also contains MDB message send and response.

2. PubSub : Publish-and-Subscribe Messaging uses JMS topic to send and receive messages.

Note: The Server and Client versions of the sample are currently the same except for the server.xml. There is a sample client server.xml in the src/main/liberty/config directory.

## Running with Maven

This project can be build with [Apache Maven](http://maven.apache.org/). The project uses [Liberty Maven Plug-in][] to automatically download and install Liberty.  Liberty Maven Plug-in is also used to create, configure, and run the application on the Liberty server.

1. To start the Liberty server, run dev mode.

    ```bash
    mvn liberty:dev
    ```

Press `Ctrl+C` to exit dev mode and stop the server.

### Application Details

Use the following steps to run the application with Maven:

[http://localhost:9124/jms11-JMSSample/JMSSampleP2P?ACTION=listAction](http://localhost:9124/jms11-JMSSample/JMSSampleP2P?ACTION=listAction)

the Topic application actions will be available under :

[http://localhost:9124/jms11-JMSSample/JMSSamplePubSub?ACTION=listAction](http://localhost:9124/jms11-JMSSample/JMSSamplePubSub?ACTION=listAction)


## Notice

© Copyright IBM Corporation 2015, 2021.

## License

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

[Liberty Maven Plug-in]: https://github.com/OpenLiberty/ci.maven
