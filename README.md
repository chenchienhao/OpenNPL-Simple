## Prueba simple de OpenNLP
Se Realiza la prueba de OpenNLP en Java con la siguiente frase:
> John Smith is standing next to bus stop and waiting for Mike.

<br>

### Crear un Proyecto Maven
```
mvn -B archetype:generate -DarchetypeGroupId=org.apache.maven.archetypes -DgroupId=com.nlp.test -DartifactId=nlp-test
```

### Ejecutar
```
mvn clean -Dget-models compile assembly:single
mvn exec:java -Dexec.mainClass="com.nlp.test.App"
java -cp target/nlp-test-1.0-SNAPSHOT.jar com.nlp.test.App
```

<br>

### Resultado Esperado
```
-------Finding entities belonging to category : person name------
[0..2) person  :  John Smith 
[11..12) person  :  Mike 

-------Finding entities belonging to category : place name------
[4..5) location  :  Atlanta 
```

OK! ;)