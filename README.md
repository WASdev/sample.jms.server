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


### Contributor License Agreement

In order for us to accept pull requests, you must declare that you wrote the code or, at least, have the right to contribute it to the repo under the open source license of the project in the repo. It's very easy...

1. Read this (from [developercertificate.org](http://developercertificate.org/)):

  ```
  Developer Certificate of Origin
Version 1.1

Copyright (C) 2004, 2006 The Linux Foundation and its contributors.
660 York Street, Suite 102,
San Francisco, CA 94110 USA

Everyone is permitted to copy and distribute verbatim copies of this
license document, but changing it is not allowed.


Developer's Certificate of Origin 1.1

By making a contribution to this project, I certify that:

(a) The contribution was created in whole or in part by me and I
    have the right to submit it under the open source license
    indicated in the file; or

(b) The contribution is based upon previous work that, to the best
    of my knowledge, is covered under an appropriate open source
    license and I have the right under that license to submit that
    work with modifications, whether created in whole or in part
    by me, under the same open source license (unless I am
    permitted to submit under a different license), as indicated
    in the file; or

(c) The contribution was provided directly to me by some other
    person who certified (a), (b) or (c) and I have not modified
    it.

(d) I understand and agree that this project and the contribution
    are public and that a record of the contribution (including all
    personal information I submit with it, including my sign-off) is
    maintained indefinitely and may be redistributed consistent with
    this project or the open source license(s) involved.
  ```

2. If you can certify that it is true, sign off your `git commit` with a message like this:
  ```
  Signed-off-by: Scott Kurz <skurz@us.ibm.com>
  ```
  You must use your real name (no pseudonyms or anonymous contributions, sorry).
  
  Instead of typing that in every git commit message, your Git tools might let you automatically add the details for you. If you configure them to do that, when you issue the `git commit` command, just add the `-s` option.

If you are an IBM employee, please contact us directly as the contribution process is slightly different.

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
