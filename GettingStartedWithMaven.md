# Getting started with maven #

## Add the repo ##

### In settings.xml ###

Add the following to your ~/.m2/settings.xml :

```
<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0
                      http://maven.apache.org/xsd/settings-1.0.0.xsd">
  ...
  <profiles>
	...
    <profile>
      <id>android-vcard-repos</id>
      <activation>
        <activeByDefault>true</activeByDefault>
      </activation>
      <repositories>
        <repository>
          <id>ossSonatype</id>
          <name>Android vcard repo (at Sonatype OSS)</name>
          <releases>
            <enabled>true</enabled>
            <updatePolicy>always</updatePolicy>
            <checksumPolicy>warn</checksumPolicy>
          </releases>
          <snapshots>
            <enabled>true</enabled>
            <updatePolicy>always</updatePolicy>
            <checksumPolicy>warn</checksumPolicy>
          </snapshots>
          <url>https://oss.sonatype.org/content/groups/public</url>
          <layout>default</layout>
        </repository>
      </repositories>
    </profile>
    ...
  </profiles>
  ...
</settings>
```

### In your project's pom.xml ###

[But it is not a good idea](http://www.sonatype.com/people/2009/02/why-putting-repositories-in-your-poms-is-a-bad-idea/)

```
<project>
    ...
    <repositories>
        ...
        <repository>
            <id>ossSonatype</id>
            <url>https://oss.sonatype.org/content/groups/public</url>
            <releases>
                <enabled>true</enabled>
            </releases>
            <snapshots>
                <enabled>true</enabled>
            </snapshots>
        </repository>
        ...
    </repositories>
    ...
</project>
```

### To your repository proxy ###

Simply add the url https://oss.sonatype.org/content/groups/public to your repository proxy (Nexus, Archiva, Artifactory...).

This repo manages both snapshots and releases and is a Maven 2 repo.

## Add the dependency to your project's pom ##

### Snapshot version ###

Add the following to your project's pom.xml :

```
<project>
    ...
    <dependencies>
        ...
        <dependency>
            <groupId>com.googlecode.android-vcard</groupId>
            <artifactId>android-vcard</artifactId>
            <version>1.3.100-SNAPSHOT</version>
        </dependency>
        ...
    </dependencies>
    ...
</project>
```

### Release version ###

A release version is not available yet in this repo. We are working on this issue and will update this page when ready.