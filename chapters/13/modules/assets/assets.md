### Todos os comandos serão executados como diretório base `assets`.

- Compilar os arquivos
```bash
javac --module-path mods -d feeding feeding/zoo/animal/feeding/Task.java feeding/module-info.java
```

- Executar o programa compilado
```bash
java --module-path feeding --module zoo.animal.feeding/zoo.animal.feeding.Task
```

- Empacotar os arquivos compilados
```bash
jar -cvf mods/zoo.animal.feeding.jar -C feeding .
```

- Executar .jar
```bash
java -p mods -m zoo.animal.feeding/zoo.animal.feeding.Task
```

