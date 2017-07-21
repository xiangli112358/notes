# Maven How To Do

## How to add non-maven JARs to a maven project
Use `maven-install-plugin` to install non-maven jars to local repository at `clean` phase.

```
<plugin>
<groupId>org.apache.maven.plugins</groupId>
<artifactId>maven-install-plugin</artifactId>
<version>${version.maven-install-plugin}</version>
<executions>
  <execution>
    <id>install-external-non-maven-jar</id>
    <phase>clean</phase>
    <configuration>
      <repositoryLayout>default</repositoryLayout>
      <groupId>non-maven</groupId>
      <artifactId>non-maven</artifactId>
      <version>${version.non-maven}</version>
      <file>${project.basedir}/libs/non-maven.jar</file>
      <packaging>jar</packaging>
      <generatePom>true</generatePom>
    </configuration>
    <goals>
      <goal>install-file</goal>
    </goals>
  </execution>
</executions>
</plugin>
```