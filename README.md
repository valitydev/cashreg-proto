# cashreg-proto

Требования к оформлению Thrift IDL файлов
Namespace:

В каждом файле нужно обязательно указывать namespace для JAVA:

```
namespace java dev.vality.damsel.<name>
```

Где `<name>` - имя, уникальное для Thrift IDL файлa.

Java development
Собрать пакет и инсталировать новый jar в локальный мавен репозиторий:

```
make wc_compile
make wc_java_install LOCAL_BUILD=true SETTINGS_XML=path_to_rbk_maven_settings
```

Чтобы ипользовать несколько версий в проекте используйте `classifier:v${commit.number}`

```
<dependency>
    <groupId>dev.vality</groupId>
    <artifactId>cashreg-proto</artifactId>
    <version>1.136-07b0898</version>
    <classifier>v136</classifier>
</dependency>
```
