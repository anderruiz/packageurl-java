[![Build Status](https://travis-ci.org/package-url/packageurl-java.svg?branch=master)](https://travis-ci.org/package-url/packageurl-java)
[![License][license-image]][license-url]

Package URL (purl) for Java
=========

This project implements a purl parser and class for Java.

Compiling
-------------------

```bash
mvn clean install
````

Maven Usage
-------------------
Package URL for Java is currently pre-release software but snapshot builds can be used and 
are available on the Maven Central Repository. These can be used without having too compile 
the project yourself.

```xml
<dependencies>
    <dependency>
        <groupId>com.github.package-url</groupId>
        <artifactId>packageurl-java</artifactId>
        <version>1.0.0-SNAPSHOT</version>
    </dependency>
</dependencies>
```

Usage
-------------------

Creates a new PURL object from a string:
```java
PURL purl = new PURL(purlString);
````

Creates a new PURL object from purl parameters:
```java
PURL purl = new PURL(type, namespace, name, version, qualifiers, subpath);
````

Access Getters and Setters:
```java
purl.setNamespace(namespace);
String subpath = purl.getSubpath();
````

Fluent interface: 
```java
purl
  .type(type)
  .namespace(namespace)
  .name(name)
  .version(version)
  .qualifiers(qualifiers)
  .subpath(subpath);
````

License
-------------------

Permission to modify and redistribute is granted under the terms of the 
[MIT License] [license-url]

  [license-image]: https://img.shields.io/badge/license-mit%20license-brightgreen.svg
  [license-url]: https://github.com/package-url/packageurl-java/blob/master/LICENSE
