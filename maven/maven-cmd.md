
## Maven CMD

Display a list of the profiles which are currently active.
>mvn help:active-profiles

Display a list of available profiles under the current project.
>mvn help:all-profiles

Display the effective POM as an XML for this build, with active profiles factored in
>mvn help:effective-pom

Display the calculated settings as XML for this project, given any porfile enhancement and the inheritance of the global settings into the user-level settings
>mvn help:effective-settings

Evaluates Maven expressions given by the user in an interactive mode
>mvn help:eveluate

Display help information on maven-help-plugin. Add -Ddetail=true and -Dgoal=_goal-name_ to display parameter details
>mvn help:help [-Ddetail=true | -Dgoal=_goal-name_]

Display a list of the platform details like system properties and environment variables
>mvn help:system

Let Maven to clear dependency artifact files out of the local repository, and optionally re-resolve them
>mvn dependency:purge-local-repository

Test single class [and single method]
>mvn -Dtest=_Test-Class_[#_Test-Methoc_][,next ...] test

Use specific local repository
>mvn -Dmaven.repo.local=\<path to local repo\> \<maven command\>

JaCoCo report (must install and config jacoco-maven-plugin in pom.xml)
>mvn jacoco:report

Display effective pom.xml
> mvn help:effective-pom