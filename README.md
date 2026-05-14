**This is the template README. Please update this with project specific content.**

# death-in-service-ui-tests

Death in Service UI journey tests.

## Pre-requisites

### Services

Start Mongo Docker container as follows:

```bash
docker run --rm -d -p 27017:27017 --name mongo percona/percona-server-mongodb:6.0
```
## Running the service

Make sure you run all the dependant services through the service manager:

```bash
> `sm2 --start DEATH_IN_SERVICE_ALL`
```

or if you want to run IHTP and DIS in parallel:

```bash
> `sm2 --start IHTP_AND_DIS_ALL`
```
## Tests

Run tests as follows:

* Argument `<browser>` must be `chrome`, `edge`, or `firefox`.
* Argument `<environment>` must be `local`, `dev`, `qa` or `staging`.



```bash
sbt clean -Dbrowser="<browser>" -Denvironment="<environment>" test testReport
```


## Scalafmt

Check all project files are formatted as expected as follows:

```bash
sbt scalafmtCheckAll scalafmtCheck
```

Format `*.sbt` and `project/*.scala` files as follows:

```bash
sbt scalafmtSbt
```

Format all project files as follows:

```bash
sbt scalafmtAll
```

## License

This code is open source software licensed under the [Apache 2.0 License]("http://www.apache.org/licenses/LICENSE-2.0.html").
