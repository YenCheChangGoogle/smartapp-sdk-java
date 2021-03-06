# java-ratpack-guice-smartapp ![java-logo](../../docs/java-logo.png) ![ratpack-logo](../../docs/ratpack-logo.png)

This sample demonstrates a simple [Java](https://www.oracle.com/java/) server using
[Ratpack](https://ratpack.io) as a web server and [Google Guice](https://github.com/google/guice))
for dependency injection.

## Requirements

* Java 1.8+
* [SmartThings developer](https://smartthings.developer.samsung.com/workspace/) account

## Running the Example

### Build and Run

Execute the following command from the project root directory:

```
./gradlew examples:java-ratpack-guice-smartapp:compileJava
./gradlew examples:java-ratpack-guice-smartapp:run
```

### Create SmartApp

Note: it is necessary for the application to be running before you create the
SmartApp in the developer console. You will need to restart once configured.

Follow these steps using the
[developer workspace](https://smartthings.developer.samsung.com/workspace/):

  1. Create a new project and choose "Automation for the SmartThings App".
  1. Give your project a unique name.
  1. Choose "Automation Connector | SmartApp" under "Develop" in the left-hand menu.
  1. Choose "WebHook Endpoint" and enter the URL of your endpoint and click "Next".
  1. Select the `r:devices:*` and `x:devices:*` scopes and click "Next".
  1. Give your application a name and hit "Save". Note that at this point, you
     will need to have the application running. (See Build and Run above.)
  1. Save the public key created to a file called `smartthings_rsa.pub` in the
     `src/main/resources` directory.
  1. Save the new project and click the "Deploy to Test" button.
  1. Restart your server (see [Build and Run](#build-and-run) above). (This is
     necessary because we added the configuration options above.)

### Install SmartApp

First, be sure to enable
[developer mode](https://smartthings.developer.samsung.com/docs/guides/testing/developer-mode.html#Enable-Developer-Mode)
in your SmartThings application to see the self-published automation.

Now you should see your SmartApp listed (near the bottom) when you add a new Automation.

## More about SmartThings

If you are not familiar with SmartThings, we have
[extensive on-line documentation](https://smartthings.developer.samsung.com/develop/index.html).

To create and manage your services and devices on SmartThings, create an account in the
[developer workspace](https://devworkspace.developer.samsung.com/).

The [SmartThings Community](https://community.smartthings.com/c/developers/) is a good place share and
ask questions.

There is also a [SmartThings reddit community](https://www.reddit.com/r/SmartThings/) where you
can read and share information.

## License and Copyright

Licensed under the [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0)

Copyright 2019 SmartThings, Inc.
