## Installation steps - JDK and Maven

**Updating system packages & Installing JDK and Maven**

```
sudo apt-get update -y

sudo apt install openjdk-11-jre -y

sudo apt-get install maven -y
```

**Verify the java installation**

```
java -version
```

**Most commonly used maven commands**

```mvn validate``` - Validates the project structure and verifies if all necessary information is available.

```mvn compile``` - Compiles the project's source code.

```mvn test``` - Runs unit tests against compiled source code.

```mvn package``` - Packages the compiled code into a distributable format (e.g., JAR, WAR).

```mvn install``` - Installs the package into the local repository for use as a dependency in other projects (.m2).

```mvn deploy``` - Deploys the package to a remote repository for sharing with other developers or environments (Push to Nexus).

```mvn clean``` - Executes the clean phase, deleting any previous build outputs.

```mvn clean package``` - Packages the compiled code into a distributable format.

**Deploy a maven build application and make it available on internet**

```
java -jar target/<application-name>.jar
```
