# Golang-containerpilot

Golang + [containerpilot](https://www.joyent.com/containerpilot) docker images for bootstrapping your [autopiloted](https://www.joyent.com/blog/applications-on-autopilot) apps

[**Dockerhub Link**](https://hub.docker.com/r/johnhof/golang-containerpilot/)

**Usage:**
```
FROM johnhof/node-containerpilot:[GOLANG-VERSION]:[CONTAINERPILOT_VERSION]

WORKDIR /go/src/app
COPY . .

RUN go-wrapper download   # "go get -d -v ./..."
RUN go-wrapper install    # "go install -v ./..."

COPY /path/to/yourcontainerpilot.json /etc/containerpilot.json
# OR
ENV CONTAINERPILOT=/path/to/your/containerpilot.json

CMD ["go-wrapper", "run"] # ["app"]
```
