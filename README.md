# Maven 

## Commands 
```bash
mvn --version
mvn archetype:generate
```
## Maven working
![](slides/2023-10-03-16-25-20.png)

pom.xml - Project Object Model

## Maven Coordinates
![](slides/2023-10-03-16-36-12.png)
<br></br>
---
![](slides/2023-10-03-16-36-31.png)

## Compiling 
`mvn compile`

## Testing and packaging
`mvn test`
`mvn package`

## Declarative Dependency Management
![](slides/2023-10-03-17-00-23.png)
[Maven repository](https://mvnrepository.com/)
1. Paste the dependency in pom.xml
2. Run `mvn dependency:copy-dependencies`

## Transitive Dependencies 
![](slides/2023-10-03-17-12-18.png)

## Maven Strategies for Transitive Dependencies
![](slides/2023-10-03-17-18-34.png)

## Dependency scopes
1. While compiling the source code, you don't need JUnit dependency, so you can mark it as `Test` scope.
2. The default scope Maven assumes is `compile` scope.
3.  - compile
    - test
    - provided (available during compile time and not available during runtime)
    - runtime (available during run time and not available compile runtime)
    - system (not often used)

## Declaring and using properties

```xml
<properties>
    <junit.version>4.12</junit.version>
</properties>

<dependencies>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>${junit.version}</version>
      <scope>test</scope>
    </dependency>
</dependencies>
```

## Maven Architecture in the Enterprise
![](slides/2023-10-12-09-59-45.png)

## Running mvn install 
`mvn package` - It will package it and generate a jar locally. 

`mvn install` - It will package it and put it to .m2 directory (local)

## The Maven build lifecycle 
![](slides/2023-10-12-10-35-08.png)

## Clean and site lifecycles 
![](slides/2023-10-12-10-38-45.png)

## Maven Plugins 
- Maven is a plugin heavy architecture. 
- Plugins are adding phases to the Maven lifecyle. 
- `mvn pluginName:phaseName`
- `mvn compiler:compile` is same as `mvn compile`
- `mvn install`
<br></br>
![](slides/2023-10-14-21-45-08.png)

## Maven Surefire Report Plugin

## Maven Code Quality Plugin

## Creating parent and child modules 
