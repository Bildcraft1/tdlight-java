<div align=center>
    <img src="./tdlight-jtdlib.png" width="256">
    <br /><br />
    <h2><b>TDLight Java</b></h2>
    <p>Complete Bot and Userbot Telegram library written in Java based on <a href="https://github.com/tdlib/td">TDLib</p>
    <a href="https://travis-ci.com/tdlight-team/tdlight-java-natives">
<img alt="Java CI" src="https://img.shields.io/github/workflow/status/tdlight-team/tdlight-java/Maven%20Package?style=flat-square)"></a>
    <a href="https://github.com/tdlight-team/tdlight-java/releases">
        <img alt="Release" src="https://img.shields.io/github/v/release/tdlight-team/tdlight-java.svg?include_prereleases&style=flat-square)">
    </a>
    <a href="https://www.ej-technologies.com/products/jprofiler/overview.html">
        <img alt="Jprofiler" src="https://local.cavallium.it/mirrors/jprofiler-logo/jprofiler-logo-badge.svg">
    </a>
</div>
<br>

# **💻 - Supported platforms**

**Java versions**: from Java 8 to Java 17

**Operating systems**: Linux, Windows, MacOS

**CPU architectures**:
- i386/x86 (Linux, Windows)
- amd64/x86_64 (Linux, Windows, OSX)
- armhf/armv7 (Linux)
- aarch64/armv8/arm64 (Linux)
- s390x (Linux)
- ppc64el/ppc64le (Linux)

**Required libraries for Linux: OpenSSL and zlib**

**Note: If you'r using OSX read down below otherwise the library won't work**

## macOS and OpenSSL
Because macOS ships with LibreSSL, wich is not compatible with TDLight-Java, you must install `openssl@1.1` using the <a href="https://brew.sh">brew package manager </a> and then linking it to `/usr/local/opt/openssl`

If you don't know how to do this, here below you can find the two commands you have to execute to get this working

```bash
brew install openssl@1.1
ln -sf /usr/local/Cellar/openssl@1.1/1.1.1l /usr/local/opt/openssl
```

# 📚 - **How to use the library**
## **Setting up the library using Maven**
If your are using Maven, put this code into your `pom.xml` file
```xml
<project>
    <repositories>
        <repository>
            <id>mchv</id>
            <name>MCHV Apache Maven Packages</name>
            <url>https://mvn.mchv.eu/repository/mchv/</url>
        </repository>
    </repositories>

    <dependencies>
        <dependency>
            <groupId>it.tdlight</groupId>
            <artifactId>tdlight-java</artifactId>
            <version>VERSION</version>
        </dependency>
        <dependency>
            <groupId>it.tdlight</groupId>
            <artifactId>tdlight-natives-linux-amd64</artifactId>
            <version>NATIVES_VERSION</version>
        </dependency>
        <!-- Include other native versions that you want, for example for windows, osx, ... -->
    </dependencies>
</project>
```
Replace `VERSION` with the latest release version, you can find it [here](https://github.com/tdlight-team/tdlight-java/releases).

Replace `NATIVES_VERSION` with the latest native version.
Make sure that you are using the correct natives version for the release that you are using.

## **Setting up the library using Gradle**
If you'r using Gradle, put this code on your `build.gradle`
```groovy
repositories {
    maven { url "https://mvn.mchv.eu/repository/mchv/" }
}
dependencies {
    implementation 'it.tdlight:tdlight-java:LATEST_VERSION'
    implementation 'it.tdlight:tdlight-natives-linux-amd64:NATIVES_VERSION'
    // Include other native versions that you want, for example for windows, osx, ...
}
```
Replace `VERSION` with the latest release version, you can find it [here](https://github.com/tdlight-team/tdlight-java/releases).

Replace `NATIVES_VERSION` with the latest native version.
Make sure that you are using the correct natives version for the release that you are using.

# ⚒️ - **Native dependencies**
To use TDLight Java you need to include one or more native dependencies:
- `tdlight-natives-linux-amd64`
- `tdlight-natives-linux-aarch64`
- `tdlight-natives-linux-x86`
- `tdlight-natives-linux-armv6`
- `tdlight-natives-linux-armv7`
- `tdlight-natives-linux-ppc64le`
- `tdlight-natives-windows-amd64`
- `tdlight-natives-osx-amd64`

## **Usage**
Simple initialization of a native TDLib client

An example on how to use TDLight Java can be found here: [Example.java](https://github.com/tdlight-team/tdlight-java/blob/master/example/src/main/java/it.tdlight.example/Example.java)

### **TDLight methods documentation**
[TdApi JavaDoc](https://tdlight-team.github.io/tdlight-docs)

### **TDLight extended features**
TDLight has some extended features compared to TDLib, that you can see on the [TDLight official repository](https://github.com/tdlight-team/tdlight#tdlight-extra-features).

# ？- **About**
## **License**
TDLight is licensed by Andrea Cavalli <andrea@cavallium.it> under the terms of the GNU Lesser General Public License 3

## **Libraries licenses**

JTDlib is licensed by Ernesto Castellotti <erny.castell@gmail.com> under the terms of the GNU Lesser General Public License 3

TDLib is licensed by Aliaksei Levin <levlam@telegram.org> and Arseny Smirnov <arseny30@gmail.com> under the terms of the Boost Software License				

OpenSSL is licensed under the terms of Apache License v2

Zlib is licensed under the terms of Zlib license
