This repository demonstrates an issue with [gradle-jaxb-plugin](https://github.com/rackerlabs/gradle-jaxb-plugin).
This plugin is unable to handle 'import' tags without a schemaLocation attribute.

Steps to reproduce:
* clone Git repo
* run `./gradlew clean xjc`

The error would look something like this:
```
Execution failed for task ':xsd-dependency-tree'.
> java.io.FileNotFoundException: /path/to/repo/gradle-jaxb-plugin-import-issue/src/main/resources/xsd (Is a directory)
```