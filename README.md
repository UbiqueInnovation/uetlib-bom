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
            <groupId>ch.uetlib</groupId>
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

## License

Except where otherwise noted, original uetlib code is licensed under the [Apache License 2.0](LICENSE). Third-party
files retain their original license terms; see [NOTICE](NOTICE) and any third-party notices in this repository.

## Public repositories

The BOM imports GeoTools and netCDF BOMs. These upstream artifacts are published through OSGeo and Unidata rather than
Maven Central, so their public release repositories are declared explicitly, with Central first. No Ubique registry
credentials are needed.
