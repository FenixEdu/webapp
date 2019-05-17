# FenixEdu Webapp

This repository is the base project used to generate a WAR file with the latest fenixedu-academic version.

You can use it to adapt it to your needs.

## Running it as is

The default database connection assumes username is `root` and password is empty.

1. start mysql on port `3306` at `localhost`
2. create database `fenixedu`
3. `mvn tomcat7:run`
4. open `http://localhost:8080/fenix` in your favourite browser


## WAR deployment

`mvn package` generates a WAR file at `target/fenix*.war` which can be deployed within tomcat.

## Configuration files

The following configuration files can be changed to suit your needs.

### Database connection properties

Database connection properties. Rely to the specific [file](src/main/resources/fenix-framework.properties) for more options.

```javascript
dbAlias = //localhost:3306/fenixedu
dbUsername = root
dbPassword = 
updateRepositoryStructureIfNeeded = true
```

### Application properties

Most relevant application properties. Rely to the specific [file](src/main/resources/configuration.properties) for more options. 

```javascript
# Full application url
application.url = http://localhost:8080/fenix

# Default System Locale. If empty falls back to java system default. Must be included in locales.supported
locale.default = pt-PT

# Locales that should be supported in ResourceBundles and other I18N mechanisms. If not specified falls back to a list with only the java system default.
locales.supported = en-GB, pt-PT
```
