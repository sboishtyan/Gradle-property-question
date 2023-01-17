# Gradle-property-question
This repo is reproducer of question about gradle property values in build scripts

### Expected Behavior
Property `a` value should be the same in both readings by `providers.gradleProperty(name)` and `property(name)`

### Current Behavior
When I read property via `property(name)` I see value from `app/gradle.properties`
When I read property via `providers.gradleProperty(name)` I see value from `gradle.properties`

### Context
I try to override some properties values by creating `gradle.properties` files in module dir.

### Steps to Reproduce
<!---
Provide a self-contained example project as an attached archive or a Github project.
You can use the following template with a Gradle GitHub action set up to showcase your problem: https://github.com/gradle/gradle-issue-reproducer
In the rare cases where this is infeasible, we will also accept a detailed set of instructions.
-->

1. Execute `./gradlew help`
2. Check output:
   ```
    > Configure project :app
    Property `a` value by `providers.gradleProperty`: in-root
    Property `a` value by `property`: in-app
   ```

### Your Environment
Gradle 7.5.1
Java 11

