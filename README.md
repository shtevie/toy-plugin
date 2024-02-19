# toy-plugin
This Maven plugin is used to find out who the developers of a Maven project are.

## Requirements
Java 17 is required to build and run this plugin.

## Install the Plugin
To install the plugin to our local repository, we run `mvn clean install` while in the root directory.

## Executing the Plugin
To run the goal for this plugin, run `mvn org.toy:toy-maven-plugin:1.0-SNAPSHOT:get-developers`. You may execute this 
plugin from this repository directly to test it out.

## Attaching the Plugin to a Project
Here is an example workflow to test it out for another Maven project.

Here is a sample project to clone: `git clone git@github.com:ltearno/pom-explorer.git`.
In the `pom.xml`, we add our plugin in the plugin section.

```
<plugins>
    <plugin>
        <groupId>com.toy</groupId>
        <artifactId>toy-maven-plugin</artifactId>
        <version>1.0-SNAPSHOT</version>
        <executions>
            <execution>
                <goals>
                    <goal>get-developers</goal>
                </goals>
            </execution>
        </executions>
    </plugin>
</plugins>
```
Then we can run the same command above or simply a `mvn clean compile`, as our plugin executes during the compile phase.