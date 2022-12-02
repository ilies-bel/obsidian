---
tag:
- intelliJ
- java
- maven
---
# Cheatsheet: Starter java
## <i class="fa-brands fa-java"></i> Java
- `echo $JAVA_HOME`  
  prints the path to your JDK.
- `nano(or vim) /etc/environement` or `nano(or vim) /etc/profile`  
  Change the path to your JDK. Usual JDKs path is `/usr/lib/jvm/...`
- `javac <your-java-file>`  
  Compile one java file.
- `java -jar <your-jar>`  
  Run some `.jar` file.
## Mavenruns unit tests?
- `mvn clean`  
  delete the `target/` directory
- `mvn compile`  
  compile source code, and put the compiled sources in `target/classes`
- `mvn test`  
  `mvn compile` + run unit tests.
- `mvn package`  
  `mvn test`, + package the `*.class` it in its distributable format (`.jar`, `.war`, ...). Artifact produced is stored in `target/`
- `mvn verify`  
  `mvn package`, + run integration tests
- `mvn install`  
  `mvn verify`, + copies the produced artifact into the local repository (usually, `~/.m2`)
- `mvn clean install -DskipTests`  
  `mvn clean` + `mvn install`, skipping tests
- `mvn deploy`  
  `mvn install`, + send the artifact to the remote repository
## IntelliJ tricks
- IntelliJ has some useful panel shortcuts all around the main window:
  - `Maven tab` (Right side): you have all lifecyle methods described above.  
    ![Maven_IntelliJ]
  - `Database tab` (Right side): Test and see your database connection.  
    ![Database_IntelliJ]
  - `Terminal tab` (Bottom): Terminal in root folder of your project.
- `Alt+Enter` on red text: Display issues causes and proposes quick-fixes.  
  ![IssueSolver_IntelliJ]
- `Ctrl+shift+F12` Close all tabs  
  ![CloseTabs_IntelliJ]
- `Ctrl+mouse`, `Ctrl+click`: Show brief info about a component and declaration when you click  
  ![Info_IntelliJ]
- `Ctrl+O`: override methods & `Ctrl+I`: implement methods  
  ![Override_IntelliJ]
- `Ctrl+/`: line comments & `Ctrl+shift+/`: block comments  
  (use / from numeric pad or qwerty keyboard)
- `Ctrl+Alt+I`: Auto indent lines  
  ![AutoIndent_IntelliJ]
- `Ctrl+Alt+O`: Remove unused imports  
  ![RemoveImport_IntelliJ]
- `Ctrl+D`: duplicate line (or selection)
- `Ctrl+Y`: Delete following line
[Maven_IntelliJ]: ../assets/cheatsheet/maven_IntelliJ.png
[Database_IntelliJ]: ../assets/cheatsheet/databaseTabIntelliJ.gif
[IssueSolver_IntelliJ]: ../assets/cheatsheet/issueSolver_IntelliJ.gif
[CloseTabs_IntelliJ]: ../assets/cheatsheet/closeTabs_IntelliJ.gif
[Override_IntelliJ]: ../assets/cheatsheet/override_IntelliJ.gif
[AutoIndent_IntelliJ]: ../assets/cheatsheet/autoIndent_IntelliJ.gif
[Info_IntelliJ]: ../assets/cheatsheet/info_IntelliJ.gif
[RemoveImport_IntelliJ]: ../assets/cheatsheet/removeImport_IntelliJ.gif