[![](https://images.microbadger.com/badges/image/tenshi/graalvm-native-image.svg)](https://microbadger.com/images/tenshi/graalvm-native-image "Get your own image badge on microbadger.com")
[![](https://images.microbadger.com/badges/version/tenshi/graalvm-native-image.svg)](https://microbadger.com/images/tenshi/graalvm-native-image "Get your own version badge on microbadger.com")

### GraalVM CE native-image as a docker container

https://hub.docker.com/r/tenshi/graalvm-native-image/

Provides a handy way to build native images for arbitrary JVM projects. Here is an example:

```bash
docker run -it -v $(pwd):/project --rm tenshi/graalvm-native-image \
  --verbose \
  -cp $CLASSPATH \
  -H:Name=app \
  -H:Class=$MAIN_CLASS \
  -H:+ReportUnsupportedElementsAtRuntime
```
