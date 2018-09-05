# Run Gatling in docker

```bash
docker pull romicaraicu/gatling-docker
```

# Clone your repo where the test suites are defined:

```bash
docker run -it -v <PATH_TO_TEST_SUITE>:/tmp romicaraicu/gatling-docker:latest sh
cd /tmp/
mvn gatling:test -Dgatling.simulationClass=<TEST_SUITE>
```

```bash
docker run -i -v "$(pwd)":/tmp -w "/tmp" romicaraicu/gatling-docker:latest mvn gatling:test -Dgatling.simulationClass=<TEST_SUITE>
```
