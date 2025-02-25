## [OPTIONAL] Confirm software version and environment variables

1. Confirm GraalVM is the current JDK:

    ```shell
    csruntimectl java list
    ```

    The output should be similar to:

    ```shell
    * graalvmeejdk-17.0.4.1                                         /usr/lib64/graalvm/graalvm22-ee-java17
      openjdk-11.0.16.1                        /usr/lib/jvm/java-11-openjdk-11.0.16.1.1-1.0.1.el7_9.x86_64
      openjdk-1.8.0.345                       /usr/lib/jvm/java-1.8.0-openjdk-1.8.0.345.b01-1.el7_9.x86_64
    ```

2. Confirm the environment variable `JAVA_HOME` is set correctly:

    ```shell
    echo $JAVA_HOME
    ```

    The output should be similar to:

    ```shell
    /usr/lib64/graalvm/graalvm22-ee-java17
    ```

3. Confirm the environment variable `PATH` is set correctly:

    ```shell
    echo $PATH
    ```

    The output should be similar to:

    ```shell
    /usr/lib64/graalvm/graalvm22-ee-java17/bin/:...
    ```

4. Confirm the `java` version:

    ```shell
    java -version
    ```

    The output should be similar to:

    ```shell
    java version "17.0.4.1" 2022-08-18 LTS
    Java(TM) SE Runtime Environment GraalVM EE 22.2.0.1 (build 17.0.4.1+1-LTS-jvmci-22.2-b08)
    Java HotSpot(TM) 64-Bit Server VM GraalVM EE 22.2.0.1 (build 17.0.4.1+1-LTS-jvmci-22.2-b08, mixed mode, sharing)s
    ```

5. Confirm the `native-image` version:

    ```shell
    native-image --version
    ```

    The output should be similar to:

    ```shell
    GraalVM 22.2.0.1 Java 17 EE (Java Version 17.0.4.1+1-LTS-jvmci-22.2-b08)
    ```

6. Confirm the `Java` used for Maven builds:

    ```shell
    mvn --version
    ```

    The output should be similar to:

    ```shell
    ...
    Java version: 17.0.4.1, vendor: Oracle Corporation, runtime: /usr/lib64/graalvm/graalvm22-ee-java17
    ...
    ```

Go back to continue with the rest of the example.
