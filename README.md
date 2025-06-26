# rama-examples

This repository contains examples from the [Rama documentation](https://redplanetlabs.com/docs/~/index.html). To see short, end-to-end, thoroughly commented examples of using Rama check out [rama-demo-gallery](https://github.com/redplanetlabs/rama-demo-gallery).

Rama currently only works on macOS or Linux and doesn't work on Windows.

As explained in the docs, you can start a Groovy REPL with:

```bash
mvn compile

# Before launching the Groovy shell, make sure your JAVA_HOME points to Java 17 or lower
# (Groovy 3.x and GMavenPlus do not support Java 18+; class file version 65 will fail).
mvn gplus:shell
```

This is a great way to run the examples or experiment.

> **Note:** Groovy REPL via GMavenPlus currently requires Java 17 or below (set JAVA_HOME accordingly).

---

## Ubuntu 24.10: Installing a supported JDK for Groovy

Ubuntu 24.10 ships with OpenJDK 21 by default, which is newer than the Java versions Groovy supports (Groovy 4.x is tested on Java 8, 11, and 17). To install and switch to OpenJDK 17:

```bash
# Ensure this is Ubuntu 24.10
if [ "$(lsb_release -rs)" = "24.10" ]; then
  echo "Detected Ubuntu 24.10 – installing OpenJDK 17 for Groovy support"

  sudo apt update
  sudo apt install -y openjdk-17-jdk

  sudo update-alternatives --install /usr/bin/java java /usr/lib/jvm/java-17-openjdk-amd64/bin/java 1
  sudo update-alternatives --install /usr/bin/javac javac /usr/lib/jvm/java-17-openjdk-amd64/bin/javac 1

  sudo update-alternatives --config java
  sudo update-alternatives --config javac
else
  echo "Not running on Ubuntu 24.10 – skipping OpenJDK 17 installation"
fi

# Verify the Java version
java -version
```

Alternatively, you can use [SDKMAN!](https://sdkman.io/) to manage Java versions per user:

```bash
curl -s "https://get.sdkman.io" | bash
source "$HOME/.sdkman/bin/sdkman-init.sh"

sdk install java 17.0.8-tem
sdk default java 17.0.8-tem
```
