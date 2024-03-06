
Mutation de test permet de valider que les tests sont efficace.
Mais l'execution est plus long

Mise en place de mutation de test avec pitest sur maven
```xml
<plugin>
  <groupId>org.pitest</groupId>
  <artifactId>pitest-maven</artifactId>
  <version>1.7.1</version>
  <!-- optional, this example attached the goal into mvn test phase
  instead of launching mvn clean test org.pitest:pitest-maven:mutationCoverage
  reports are found under target/pi-reports
  -->
  <executions>
    <execution>
      <id>pit-report</id>
      <phase>test</phase>
      <goals>
        <goal>mutationCoverage</goal>
      </goals>
    </execution>
  </executions>
  <configuration>
    <timestampedReports>false</timestampedReports>
  </configuration>
  <!-- https://github.com/hcoles/pitest/issues/284 -->
  <!-- Need this to support JUnit 5 -->
  <dependencies>
    <dependency>
      <groupId>org.pitest</groupId>
      <artifactId>pitest-junit5-plugin</artifactId>
      <version>0.15</version>
    </dependency>
  </dependencies>
</plugin>
```

---

Source:
- https://pitest.org/quickstart/maven/
