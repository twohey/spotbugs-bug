# Reproduction Steps

run `mvn -e verify` and see output that has an error

```
[INFO] >>> spotbugs-maven-plugin:3.0.6:check (spotbugs-check) > :findbugs @ spotbugs-1 >>>
[INFO]
[INFO] --- spotbugs-maven-plugin:3.0.6:findbugs (findbugs) @ spotbugs-1 ---
[INFO] ------------------------------------------------------------------------
[INFO] BUILD FAILURE
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 2.573 s
[INFO] Finished at: 2017-10-08T20:06:46-04:00
[INFO] Final Memory: 16M/53M
[INFO] ------------------------------------------------------------------------
[ERROR] 9897
java.lang.ArrayIndexOutOfBoundsException: 9897
    at org.codehaus.plexus.util.xml.pull.MXParser.parsePI(MXParser.java:2502)
    at org.codehaus.plexus.util.xml.pull.MXParser.parseEpilog(MXParser.java:1604)
    at org.codehaus.plexus.util.xml.pull.MXParser.nextImpl(MXParser.java:1434)
    at org.codehaus.plexus.util.xml.pull.MXParser.next(MXParser.java:1131)
...
```


# System Information

```
% java -version
java version "9"
Java(TM) SE Runtime Environment (build 9+181)
Java HotSpot(TM) 64-Bit Server VM (build 9+181, mixed mode)
```

```
% uname -a
Darwin twohey-book.local 17.0.0 Darwin Kernel Version 17.0.0: Thu Aug 24 21:48:19 PDT 2017; root:xnu-4570.1.46~2/RELEASE_X86_64 x86_64
```
