# Gradle Eclipse plugin with WSL
Windows has created the so called [Windows Subsystem for Linux](https://docs.microsoft.com/es-es/windows/wsl/about), which is a almost real Linux OS.
Seems to be giving better support than Cygwin or similars.

Building with Gradle inside the OS selected (you can even install multiple Unix based OS's!) works like a charm, but when trying to use the project's inside my prefered IDE, Eclipse, the path mappings to libraries are broken.

This repository is a really simple example that when selecting task `eclipse`, the `.classpath` created is created using Linux path's.
The path's I got, using `GRADLE_USER_HOME="/mnt/d/Users/Luc/Downloads/develop/.gradle"`, are like:
```
/mnt/d/Users/Luc/Downloads/develop/.gradle/...
```

instead of:
```
D:/Users/Luc/Downloads/develop/.gradle/...
```
That I would got using Cygwin (or Windows native (?)).

So Eclipse does not recognize, and can't use the dependencies downloaded.
