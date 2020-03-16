# fastapi-service-wizard
A template for building a buildyio service using fastapi and openapi standards


## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

* Docker version 19+

### Installing

Build first the image:

* Go to the project directory (in where your `Dockerfile` is, containing your `app` directory).
* Build your FastAPI image:

```bash
docker build -t myimage .
```

* Run a container based on your image:

```bash
docker run -d --name mycontainer -p 80:80 myimage
```

## Running the tests



## Deployment

The instructions in the next three subsections [Configure the API authentication](#configure-the-api-authentication), [Generating RSA keys](#generating-rsa-keys), and [Configuration](#configuration) will explain how to configure a Buildly Core instance to have it on a live system.


### Configuration

The following table lists the configurable parameters of buildly and their default values.

|             Parameter               |            Description             |                    Default                |
|-------------------------------------|------------------------------------|-------------------------------------------|
| `DATABASE_ENGINE`                   | The database backend to use. (`postgresql`, `mysql`, `sqlite3` or `oracle`) | `` |
| `DATABASE_NAME`                     | The name of the database to use          | ``                                  |
| `DATABASE_USER`                     | The username to use when connecting to the database | ``                       |
| `DATABASE_PASSWORD`                 | The password to use when connecting to the database | ``                       |
| `DATABASE_HOST`                     | The host to use when connecting to the database | ``                           |
| `DATABASE_PORT`                     | The port to use when connecting to the database | ``                           |
| `DEFAULT_ORG`                       | The first organization created in the database  | `My Organization`            |

Specify each parameter using `-e`, `--env`, and `--env-file` flags to set simple (non-array) environment variables to `docker run`. For example,

```bash
$ docker run -e MYVAR1 --env MYVAR2=foo \
    --env-file ./env.list \
    buildly/buildly:<version>
```

## Built With

* [Travis CI](https://travis-ci.org/) - Recommended CI/CD

## Contributing

Please read [CONTRIBUTING.md](https://github.com/buildlyio/docs/blob/master/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/buildlyio/buildly-core/tags).

## Authors

* **Buildly** - *Initial work*

See also the list of [contributors](https://github.com/buildlyio/buildly-core/graphs/contributors) who participated in this project.

## License

This project is licensed under the GPL v3 License - see the [LICENSE](LICENSE) file for details.
