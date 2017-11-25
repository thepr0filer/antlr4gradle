# antlr4gradle
Template gradle project for use with antlr, integrated via a custom gradle task

* As an example, the src/lang folder includes the JSON grammar from https://github.com/antlr/grammars-v4/tree/master/json
* Based on the properties in gradle.properties, the *generateLang* task upon which the build task is dependent will be
generating the Java classes in the corresponding packages/paths. task *cleanLang* will remove all generated files from 
the output directory

## Example

### Input
gradle.properties
* rootProject.name = 'antlr4gradle'
* rootProjectNameSpace = eu.dragulescu

settings.gradle
* rootProjectGrammarName = JSON

### Output
- will read the grammar from: src/main/lang/JSON.g4
- will generate output into : src/main/java/eu/dragulescu/antlr4gradle/lang/JSON/
- the classes will be declared in package eu.dragulescu.antlr4gradle.lang.JSON

