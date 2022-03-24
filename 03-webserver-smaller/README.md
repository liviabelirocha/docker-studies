### To build:

`$ docker build -t="webserver-smaller" .`

### To run:

`$ docker run -d -p 80:80 webserver-smaller`

This Dockerfile contains one extra command comparing to `02`, but still fewer layers.
You can check it with:

`$ docker history webserver-smaller`
