# Antの利用法 [ for macOS ]

## 利用環境
1. OS : macOS 10.12.3
2. Javac : 1.8.0_112
3. Java : 1.8.0_112
4. Ant : 1.10.1

## インストール
```
$ brew install ant
```

## サンプルソース [ Hello.java ]
```
public class Hello {
  public static void main(String[] args) {
    System.out.println("Hello World.");
  }
}
```

## 設定ファイル [ build.xml ]
```
<project name="Hello" default="build">
  <target name="build">
    <javac srcdir="." includeantruntime="false" />
    <java classname="Hello" classpath="." />
  </target>
</project>
```

## 実行結果
```
$ ant
Buildfile: /Users/ht0919/java/build.xml

build:
    [javac] Compiling 1 source file
     [java] Hello World.

BUILD SUCCESSFUL
Total time: 1 second
```
