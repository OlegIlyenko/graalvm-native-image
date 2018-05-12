### GraalVM native-image as a docker container

Provides a handy way to build native images for arbitrary JVM projects. Here is an example:

```bash
docker run -it -v $(pwd):/project --rm tenshi/graalvm-native-image \
  --verbose \
  -cp $CLASSPATH \
  -H:Name=app \
  -H:Class=$MAIN_CLASS \
  -H:+ReportUnsupportedElementsAtRuntime
```