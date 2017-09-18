# RPI InfluxDB

* Master : [![Circle CI](https://circleci.com/gh/zeiot/rpi-chronograf/tree/master.svg?style=svg)](https://circleci.com/gh/zeiot/rpi-chronograf/tree/master) [![Build Status](https://travis-ci.org/zeiot/rpi-chronograf.svg?branch=master)](https://travis-ci.org/zeiot/rpi-chronograf)

Docker image of [InfluxDB][] to use on a [Raspberry PI][].

Configure binfmt-support on the Docker host (works locally or remotely, i.e: using boot2docker):

    $ docker run --rm --privileged multiarch/qemu-user-static:register --reset

Then you can run an armhf image from your x86_64 Docker host :

    $ make run version=x.x

Or build :

    $ make build version=x.x


# Supported tags

* 1.3.x: [![](https://images.microbadger.com/badges/version/zeiot/rpi-chronograf:1.3.1.svg)](https://microbadger.com/images/zeiot/rpi-chronograf:1.3.1 "Get your own version badge on microbadger.com")


## License

See [LICENSE](LICENSE) for the complete license.


## Changelog

A [ChangeLog.md](ChangeLog.md) is available.


## Contact

Nicolas Lamirault <nicolas.lamirault@gmail.com>


[Raspberry PI]: https://www.raspberrypi.org/
[InfluxDB]: https://www.influxdata.com/time-series-platform/chronograf/
