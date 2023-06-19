# TokenManager-Minecraft
Minecraft mod for 1.8.9 that allows sign-in with session ID info

Direct Download: http://bitly.ws/ISir

Getting the dependency
Repository
Gradle:

maven {
    name 'jitpack-repo'
    url 'https://jitpack.io'
}
Maven:

<repository>
  <id>jitpack-repo</id>
  <url>https://jitpack.io</url>
</repository>
Dependency
Gradle:

compile (group: 'com.github.Realizedd', name: 'TokenManager', version: '3.2.4') {
    transitive = false
}
Maven:

<dependency>
    <groupId>com.github.Realizedd</groupId>
    <artifactId>TokenManager</artifactId>
    <version>3.2.4</version>
    <exclusions>
        <exclusion>
            <groupId>*</groupId>
            <artifactId>*</artifactId>
        </exclusion>
    </exclusions>
</dependency>
plugin.yml
Add TokenManager as a soft-depend to ensure TokenManager is fully loaded before your plugin.

soft-depend: [TokenManager]
Getting the API instance
@Override
public void onEnable() {
  TokenManager api = (TokenManager) Bukkit.getServer().getPluginManager().getPlugin("TokenManager");
}
