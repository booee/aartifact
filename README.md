# aartifact

> An small utility to help you generate an android artifact `.aar` with an appropriate `pom.xml` with dependencies

## Setup

In your library module's `build.gradle`

```

apply from: 'https://raw.githubusercontent.com/brad-bowie/aartifact/master/aartifact.gradle'

ext {
    ...
    aartifact = [
            group: 'com.your.group',
            version: '0.1.0'
    ]
}
```

## Publishing

This gradle script utilizes the `maven-publish` plugin, so it will utilize the same publishing mechanism

Example:
```
$ ./gradlew clean build publishToMavenLocal
```
