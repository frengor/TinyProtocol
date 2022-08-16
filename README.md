# TinyProtocol (fren_gor)

[TinyProtocol](https://github.com/dmulloy2/ProtocolLib/tree/master/TinyProtocol/src/main/java/com/comphenix/tinyprotocol) updated to last Spigot version.

**Distributed with maven:**
```xml
<repositories>
    <repository>
        <id>fren_gor</id>
        <url>https://nexus.frengor.com/repository/public/</url>
    </repository>
</repositories>
```
```xml
<dependency>
    <groupId>com.frengor</groupId>
    <artifactId>tinyprotocol</artifactId>
    <version>1.1-SNAPSHOT</version>
    <scope>compile</scope>
</dependency>
```

**It's suggested to shade it:**
```xml
<plugin>
    <groupId>org.apache.maven.plugins</groupId>
    <artifactId>maven-shade-plugin</artifactId>
    <version>3.3.0</version>

    <configuration>
        <relocation>
            <pattern>com.comphenix.tinyprotocol</pattern>
            <shadedPattern>your.shaded.path.com.comphenix.tinyprotocol</shadedPattern>
        </relocation>
    </configuration>

    <executions>
        <execution>
            <phase>package</phase>
            <goals>
                <goal>shade</goal>
            </goals>
        </execution>
    </executions>
</plugin>
```
