maven-repository
================

A maven repository for dependencies that are not hosted public.

The [Apache Maven Install Plugin](http://maven.apache.org/plugins/maven-install-plugin/usage.html) can be used to
install artifacts to this repository. The snippet below can be used to install the artifacts as well as the source
 artifacts.

```bash
mvn install:install-file \
 -DlocalRepositoryPath=[path-to-local-clone-of-this-git-repo] \
 -DgroupId=[group-id] \
 -DartifactId=[artifact-id] \
 -Dversion=[version] \
 -Dpackaging=[packaging-format] \
 -Dfile=[path-to-file]
```

```bash
mvn install:install-file \
 -DlocalRepositoryPath=[path-to-local-clone-of-this-git-repo] \
 -DgroupId=[group-id] \
 -DartifactId=[artifact-id] \
 -Dversion=[version] \
 -Dpackaging=[packaging-format] \
 -Dclassifier=sources \
 -Dfile=[path-to-file]
```


This repository can be used in any maven project by adding the repository to the POM file of the project.

```bash
<repositories>
  <repository>
    <id>git-GeBeater</id>
    <name>GeBeater\'s Git based repo</name>
    <url>https://github.com/GeBeater/maven-repository/raw/master/</url>
  </repository>
</repositories>
```
