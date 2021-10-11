# Instructions to deploy the server and the client

First of all, you need to have Java 11 JDK installed in your 
computer and use that version of Java to build both applications
and avoid possible errors. In order to be able of running the
`server` and the `client`, the first thing you need to do is to
build and execute the `server`. You need to execute these 
commands:

```bash
./gradlew :server:build 
./gradlew :server:bootRun
```

Once the `server` is executed, the `client` can download the 
dependencies from the wsdl file to build and execute. You need to execute these
commands:

```bash
./gradlew :client:build 
./gradlew :client:bootRun
```

However, the endpoint of the `server` isn't complete. To 
complete it, I had to complete the function called `translation`
to return a `TranslationResponse` object containing the string
"¡Tradúceme!".