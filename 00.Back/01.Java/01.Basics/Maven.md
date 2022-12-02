Cheatsheet : [[00.Back/00.Cheatsheet/Maven]]
```
mvn -B archetype:generate \
  -DarchetypeGroupId=org.apache.maven.archetypes \
  -DgroupId=io.takima.master3 \
  -DartifactId=ma-store
```
https://maven.apache.org/guides/getting-started/

Permet la generation d'un projet qui suit les conventions de maven

Lifecylce : 
chaque commande du lifecycle appelle automatiquement les précédentes 
