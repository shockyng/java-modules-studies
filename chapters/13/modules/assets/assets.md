### Todos os comandos serão executados como diretório base `assets`.

## Módulo Feeding

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

## Módulo Care
- Compilar os arquivos
```bash
javac -d care -p mods care/zoo/animal/care/details/*.java care/zoo/animal/care/medical/*.java care/module-info.java
```

- Empacotar os arquivos compilados
```bash
jar -cvf mods/zoo.animal.care.jar -C care .
```

## Módulo Schedule
- Compilar os arquivos
```bash
javac -d talks -p mods talks/zoo/animal/talks/content/*.java talks/zoo/animal/talks/media/*.java talks/zoo/animal/talks/schedule/*.java talks/module-info.java 
```

- Empacotar os arquivos compilados
```bash
jar -cvf mods/zoo.animal.talks.jar -C talks .
```

- Executar .jar
```bash
java -p mods -m zoo.animal.talks/zoo.animal.talks.media.Announcement
```

## Módulo Staff
- Compilar os arquivos
```bash
javac -d staff -p mods staff/zoo/staff/*.java staff/module-info.java
```

## Service

- Compilar os arquivos
```bash
javac -d ServiceProviderInterfaceModule ServiceProviderInterfaceModule/zoo/tours/api/*.java ServiceProviderInterfaceModule/module-info.java
```

- Empacotar os arquivos compilados
```bash
jar -cvf mods/zoo.tours.api.jar -C ServiceProviderInterfaceModule .
```

## Módulo Service Locator
- Compilar os arquivos
```bash
javac -p mods -d serviceLocatorModule serviceLocatorModule/module-info.java serviceLocatorModule/zoo/tours/reservations/TourFinder.java
```

- Empacotar os arquivos compilados
```bash
jar -cvf mods/zoo.tours.reservations.jar -C serviceLocatorModule .
```
