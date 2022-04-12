# Gradle
## Depend on other Gradle Project
In case you want to use an other of your projects as a dependency in your current projects you just need to add some few little lines to your project configuration files.

First include your other project in your current projects `settings.gradle`:
```
include ':<other project name>'
project(':<other project name>').projectDir = new File('<other project directory')
```

You can extract the project name from the `settings.gradle` file of the project you want to include. The directory should be the diskpath where the other project is located. This can also be a relative path (e.g. ../otherproject)

Then add the project to your `build.gradle`:
```
dependencies {
 implementation project(':<your-project-name>')
}
```

> Notice: the example uses `implementation` inside the `build.gradle` dependencies. This might differ depending on your project