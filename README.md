# I want to integrate a Fafner project into my project ¿How I can do this?
Maybe you got here because you're finding a Fafner project artifacts or a maven repository fields.
Actually, Fafner doesn't have a hosted maven repository or access to publishing to Maven Central.

All Fafner projects are built using Gradle. So, you have three options:
* Fork the project repository and:
  * If you're using Maven, execute the task _publishToMavenLocal_, this will generate a jar into your maven local repo.
  * If you're using Gradle you can include the project as a [included build](https://docs.gradle.org/current/userguide/composite_builds.html).
* Some Fafner project repositories publish packages (artifacts) to the Apache Maven Registry so you can take and include them with Gradle or Maven. But, this way requires authentication. [How authenticate into Apache Maven Registry](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-apache-maven-registry)
* Add it using Git submodules.
