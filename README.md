# dependencies-maven-plugin
This plugin scans your project dependencies and adds them to a file called "dependencies.properties" in "target/classes".
```
<plugin>
	<groupId>de.fegbers</groupId>
	<artifactId>dependencies-maven-plugin</artifactId>
	<version>0.1.0-RC</version>
	<executions>
		<execution>
			<phase>initialize</phase>
			<goals>
				<goal>save</goal>
			</goals>
		</execution>
	</executions>
</plugin>
```
An example output:
```
#Generated by dependency-maven-plugin
#Sat Aug 11 13:38:54 CEST 2018
dependency_org_powermock_powermock-api-easymock_jar=1.7.3
dependency_org_apache_commons_commons-lang3_jar=3.7
dependency_org_glassfish_jersey_inject_jersey-hk2_jar=2.26
dependency_com_spotify_docker-client_jar=8.9.0
dependency_org_easymock_easymock_jar=3.5.1
dependency_pl_project13_maven_git-commit-id-plugin_jar=2.2.4
dependency_org_powermock_powermock-module-junit4_jar=1.7.3
dependency_org_projectlombok_lombok_jar=1.16.22
dependency_org_assertj_assertj-core_jar=3.9.1
dependency_org_springframework_boot_spring-boot-starter-web_jar=2.0.4.RELEASE
dependency_junit_junit_jar=4.12
```
To execute this plugin you have to call the goal "save".
``` bash
//only execute the plugin
mvn de.fegbers:dependencies-maven-plugin:save
```
``` bash
//also executable via package 
 mvn clean package
```
