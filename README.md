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
