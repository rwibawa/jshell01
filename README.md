# jshell
* [Java Stream Reduce](https://www.baeldung.com/java-stream-reduce)

## 1. Setup
```bash
$ jenv global 16.0.2
$ export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk-16.0.2.jdk/Contents/Home
$ java -version
java version "16.0.2" 2021-07-20
Java(TM) SE Runtime Environment (build 16.0.2+7-67)
Java HotSpot(TM) 64-Bit Server VM (build 16.0.2+7-67, mixed mode, sharing)

```

## 2. java interactive
```bash
$ jshell 
|  Welcome to JShell -- Version 16.0.2
|  For an introduction type: /help intro

jshell> int[] nums = IntStream.range(1, 100).toArray();
nums ==> int[99] { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12,  ... , 94, 95, 96, 97, 98, 99 }

jshell> Arrays.stream(nums).reduce(0, (acc, cur) -> acc + cur);
$2 ==> 4950

jshell> List<String> words = Arrays.asList("lorem", "ipsum", "dolor", "sit", "amet", "lorem", "ipsum", "lorem");
words ==> [lorem, ipsum, dolor, sit, amet, lorem, ipsum, lorem]

jshell> /exit
|  Goodbye
```
