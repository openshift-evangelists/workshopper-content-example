# Example workshop

Workshop content designed to be used by the [Workshopper tool](https://github.com/osevg/workshopper).

# Run Guides Locally
```
$ git clone https://github.com/openshift-evangelists/workshopper-content-example
$ cd workshopper-content-example

$ docker run -it --rm -p 8080:8080 -v $(pwd):/app-data \
              -e CONTENT_URL_PREFIX="file:///app-data" \
              -e LOG_TO_STDOUT=true \
              -e WORKSHOPS_URLS="file:///app-data/_workshop.yml" \
              -e MASTER_URL="https://master.myveryownexample.com" \
              -e API_URL="https://apiserver.myveryownexample.com:6443" \
              quay.io/osevg/workshopper:stable
```
