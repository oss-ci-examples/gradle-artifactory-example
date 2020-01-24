# Sample Java Gradle project with OSS automation

Sample Java Gradle project with automation set up to publish to a public repository (Artifactory).

The sample is a multi-project build with inter-project dependency (impl -> api). 

The build uses following plugins:
 - 'java-library' - https://docs.gradle.org/current/userguide/java_library_plugin.html
 - 'maven-publish' - https://docs.gradle.org/current/userguide/publishing_maven.html
 - 'com.jfrog.artifactory' - https://www.jfrog.com/confluence/display/RTF/Gradle+Artifactory+Plugin
 
## Usage

### Publishing to ~/local-repo

Useful for local testing, when another project consumes artifacts of this project.

```./gradlew publishToLocalRepo```

### Publishing to remote Artifactory

 - export 'ARTIFACTORY_USER' AND 'ARTIFACTORY_KEY' environment variables
 - run ```./gradlew artifactoryPublish```   