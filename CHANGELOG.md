# CHANGELOG

## 2026.11.5

- Build pull requests, including forks, and pushes to `main` instead of every branch push; use shared Maven
  workflows at `v1.1.1`.
- Use shared Maven workflows at `v1.1.0`: wait for the SonarCloud quality gate and analyse with the
  uetlib-only Sonar token.
- Use shared Maven build and publish workflows at `v1.0.0` to enforce formatting checks in CI.
- Restore the Apache-2.0 license, notice, contribution and security guidance, public POM metadata and public
  upstream repositories that an earlier merge had removed.
- Request Central publication of stable releases from the uetlib entry repository after staging, once the uetlib
  release App is configured (proof of concept).

## 2026.11.4

- Clarify configuration-property migration guidance for consumers.

## 2026.11.1

- Move Java packages and class references from `ch.ubique.uetlib` to `ch.uetlib`.

## 2026.11.0

### Breaking changes

- Move Java packages from `ch.ubique.backend` to `ch.uetlib`, including class-name resources. The combined OpenRewrite
  migration also renames known Spring configuration keys to `ch.uetlib.*`.
- Remove the inherited Ubique Artifactory repository and deployment destination; private consumers must configure their
  own registry.
- Add Apache-2.0 licensing for original code, preserve third-party licenses, and add public project metadata and
  contribution/security guidance.

- Move Maven coordinates from `ch.ubique:uetlib-*` to `ch.uetlib:uetlib-*`.
- Align uetlib parent, BOM and library references with the migration releases.

### Migration

After the migration releases and `uetlib-rewrite` are published, run this from the consuming project, then review
the diff and run its tests:

```sh
mvn -U org.openrewrite.maven:rewrite-maven-plugin:6.46.1:run \
  -Drewrite.recipeArtifactCoordinates=ch.uetlib:uetlib-rewrite:RELEASE \
  -Drewrite.activeRecipes=ch.uetlib.MigrateToPublicUetlib
```

The recipe updates Maven coordinates/versions, Java references and known class-name resources. Review application-owned
packages under the old namespace, Kotlin, reflection patterns, native-access module flags and persisted class names
separately. Use `:dryRun` instead of `:run` to preview a patch.

## 2026.10.0

- Version updates

## 2026.9.2

- Version updates for `twelvemonkeys`, `kotlin`, `aws-sdk`, `springdoc`

## 2026.9.1

- Version updates

## 2026.9.0

- Version updates
- Updated github actions

## 2026.8.4

- Update `de.westemeyer:artifact-version-service` to `3.0.0`
- Add version management for `de.westemeyer:artifact-version-service-spring-boot` as `3.0.0`
- Version updates

## 2026.8.3

- Updated `de.westemeyer:artifact-version-service` to `2.1.0`, which is now null-marked
- Version updates

## 2026.8.2

- Version updates

## 2026.8.1

- Version updates
- Manage version of `net.postgis:postgis-jdbc`

## 2026.8.0

- Java 25 required

## 2026.7.6

- Set `kotlin.version` as a property so projects can override it

## 2026.7.5

- updated actions to not run tests twice for sonar

## 2026.7.4

- Version updates

## 2026.7.3

- Back to SemVer-compatible CalVer. No 0-padded months

## 2026.07.2

- Fix the url for Unidata All repository, see https://artifacts.unidata.ucar.edu/#/all/

## 2026.07.1

- Add dependency management for `com.google.errorprone:error_prone_core` and `com.uber.nullaway:nullaway`
- Updated `tomcat`, `logback`, `aws-sdk`, `sentry`, `kubernetes:client-java`
- Updated github actions

## 2026.07.0

- Reordered dependencyManagement boms as they should be. Higher up imported boms take precedence, while exact pinned
  versions below can override.
- Updated `sentry`, `logback` and `netcdf`

## 2026.06.0

- Prepared for Spring Boot 4.1
- Latest versions of all dependencies
- Moved `spring-integration-bom` version management from `uetlib-bom` to `uetlib-parent`
- updated GeoTools from `34` to `35`

## 2026.4.0

- manage versions for `io.swagger.core.v3:swagger-core/annotations/models-jakarta`, not just `annotations`
  (unfortunately, there is no BOM for this, yet)

## 2026.3.0

- latest updates for March 2026

## 2026.2.3

- Add new `de.westemeyer:artifact-version-service-sping-boot:2.0.0`

## 2026.2.0

- latest updates for February 2026
- Upgrade `de.westemeyer:artifact-version-maven-plugin` to `2.0.0`

## 2026.0.0

We adopt Calendar versioning (CalVer) `yyyy.MM.PATCH`

### Version Upgrades

- Upgrade to SpringDoc 3.0.0 for Spring Boot 4 support
- Upgrade to Spring-Integration 7.0.0 for Spring Boot 4 support

## 1.3.2

### Improvements

- add `com.squareup.okhttp3:okhttp-bom` to dependency management

## 1.3.1

### Improvements

- add `ch.ubique:inotify` to dependency management

## 1.3.0

### Improvements

- Reorder dependencyManagement from least to highest privilege. At least the boms at the top, specific versions below.

## 1.2.14

### Improvements

- Latest spring-integration version

## 1.2.13

### Improvements

- Use the new gt-bom for geotools
- Upgrade geotools to 34

## 1.2.12

### Improvements

- Newer `testcontainers-redis` versions are under a new group id.

## 1.2.11

### Improvements

- Add `commons-csv`

## 1.2.10

### Improvements

- Add `testcontainers-redis`

## 1.2.9

### Improvements

- Replace bouncycastle versions with new BOM `bc-jdk18on-bom`
- Renovate version updates

## 1.2.8

### Improvements

- Renovate version updates

## 1.2.7

### Improvements

- Renovate version updates

## 1.2.6

### Improvements

- Renovate version updates

## 1.2.5

### Improvements

- Add `kotlin-bom`
- Renovate version updates

## 1.2.4

### Improvements

- Add `jackson-bom`
- Renovate version updates

## 1.2.3

### Improvements

- Add `commons-fileupload` as a managed version

## 1.2.2

### Improvements

- Include `com.twelvemonkeys.bom:bom` instead of only `com.twelvemonkeys.imageio:imageio-jpeg`

## 1.2.1

### Improvements

- Latest uetlib dependencies with Spring Boot 3.5 / Spring Cloud 2025.0.0

## 1.2.0

- Dependency updates
- Added more boms

## 1.1.0

- Dependency updates

## 1.0.0

First release.

