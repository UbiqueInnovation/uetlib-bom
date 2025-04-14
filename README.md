# Uetlib BOM

Bill of Materials maven POM for uetlib libraries.

This project specifies **the third-party dependencies** of `uetlib`.
The versions of the `uetlib-*` modules are specified
in [`uetlib-self-bom`](https://github.com/UbiqueInnovation/uetlib-self-bom).

## Using

### As dependencyManagement

You can use this artifact as dependencyManagement for your maven project.
You can use it as following:

```xml

<dependencyManagement>
    <dependencies>
        <dependency>
            <groupId>ch.ubique</groupId>
            <artifactId>uetlib-bom</artifactId>
            <version>{latest}</version>
            <type>pom</type>
            <scope>import</scope>
        </dependency>
    </dependencies>
</dependencyManagement>
```

## Changelog

See [CHANGELOG.md](CHANGELOG.md)
