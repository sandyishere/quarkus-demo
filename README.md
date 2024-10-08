# quarkus demo

demonstrates creating a new quarkus app bootstrapped with rest extension.

following tutorial from: https://quarkus.io/guides/maven-tooling#project-creation

## create new project

```
mvn io.quarkus.platform:quarkus-maven-plugin:3.11.0:create \
    -DprojectGroupId=my-groupId \
    -DprojectArtifactId=my-artifactId
    -Dextensions='rest'

cd my-artifactId/
```

## run the app (hot-reload available)

```
mvn quarkus:dev
```

your app is now running on http://localhost:8080/

## test rest endpoint

```
curl http://localhost:8080/hello
```

## other useful info

### to list extensions

```
mvn quarkus:list-extensions
```

### to add extension

for example, rest:

```
mvn quarkus:add-extension -Dextensions="io.quarkus:quarkus-rest"
```
