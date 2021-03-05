Test Dependency Resolution
=============

run with:

```
\rm -rf local && mvn -s settings.xml jar:jar
```


look particularly at dependencies resolution log:

```
[INFO] 
[INFO] -----------------------------< test:deps >------------------------------
[INFO] Building Test dependencies resolution 1.0.0-SNAPSHOT
[INFO] --------------------------------[ jar ]---------------------------------
Downloading from central: https://repo.maven.apache.org/maven2/junit/junit/4.13.1/junit-4.13.1.pom
Downloaded from central: https://repo.maven.apache.org/maven2/junit/junit/4.13.1/junit-4.13.1.pom (25 kB at 1.9 MB/s)
Downloading from central: https://repo.maven.apache.org/maven2/org/hamcrest/hamcrest-core/1.3/hamcrest-core-1.3.pom
Downloaded from central: https://repo.maven.apache.org/maven2/org/hamcrest/hamcrest-core/1.3/hamcrest-core-1.3.pom (766 B at 85 kB/s)
Downloading from central: https://repo.maven.apache.org/maven2/org/hamcrest/hamcrest-parent/1.3/hamcrest-parent-1.3.pom
Downloaded from central: https://repo.maven.apache.org/maven2/org/hamcrest/hamcrest-parent/1.3/hamcrest-parent-1.3.pom (2.0 kB at 197 kB/s)
Downloading from central: https://repo.maven.apache.org/maven2/junit/junit/4.13.1/junit-4.13.1.jar
Downloading from central: https://repo.maven.apache.org/maven2/org/hamcrest/hamcrest-core/1.3/hamcrest-core-1.3.jar
Downloaded from central: https://repo.maven.apache.org/maven2/org/hamcrest/hamcrest-core/1.3/hamcrest-core-1.3.jar (45 kB at 1.6 MB/s)
Downloaded from central: https://repo.maven.apache.org/maven2/junit/junit/4.13.1/junit-4.13.1.jar (383 kB at 8.7 MB/s)
```

logs before are plugins resolution without their dependencies, logs after are maven-jar-plugin dependencies resolution
