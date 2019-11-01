# gradle-kotlin-dsl-cheat-sheet
Quick cheat sheet for migrating gradle build script to kotlin dsl 

### Gradle wrapper version
```
//gradle.properties
distributionUrl=https\://services.gradle.org/distributions/gradle-5.x.x-all.zip
```
Requires version 5.x or later.

### String quotation mark
before
```
apply plugin: 'com.android.application'
```

after
```
apply plugin: "com.android.application"
```
https://kotlinlang.org/docs/reference/basic-types.html#string-literals

### Function call
before
```
    targetSdkVersion 28
    implementation 'library.package.name'
    testFunction "value1" true
```

after
```
    targetSdkVersion(28)
    implementation("library.package.name")
    testFunction "value1" true
```
Kotlin can omit curly bracket only in lambda expressions.
Kotlin cannot omit comma in function call.
