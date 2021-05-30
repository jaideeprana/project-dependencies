# project-dependencies
A gradle multi-module project with project dependencies

## Overview
The project is created by following the official gradle guide [here](https://docs.gradle.org/current/userguide/declaring_dependencies_between_subprojects.html#declaring_dependencies_between_subprojects).

While building the project after following the steps mentioned in the guide, there was one error that I encountered.
But it was fixed by following the following steps:

1. Open the file `buildSrc/build.gradle` in your editor of choice.
1. Add the following content and save:

```groovy
plugins {
    id 'groovy-gradle-plugin'
}
```

The file called `buildSrc/src/main/groovy/myproject.java-conventions.gradle` declares what is called a precompiled script plugin.  
For this to work, you have to apply the plugin called groovy-gradle-plugin (for Groovy plugins) in the buildSrc project.

After this, it should be able to find your custom myproject.java-conventions plugin.
