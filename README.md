# cf-recycle-plugin

This Cloudfoundry cli plugin is to allow the recycling of application instances without interruption to the application availability.

The plugin works by restarting individual Application Instances(AI's) waiting for one to fully restart before moving on to the next.

### Prerequisites
The plugin was built and tested using the below versions
1. Golang 1.10.0
2. CloudFoundry CLI 6.35.2

### Installation from Source
Using your favorite versioning system, set variables for the major, minor, and patch versions.
```sh
git clone git@github.com:comcast/cf-recycle-plugin.git
go get github.com/cloudfoundry/cli
govendor build -ldflags "-X main.Major=${major} -X main.Minor=${minor} -X main.Patch=${patch}" -o out/cf-recycle-plugin cf_recycle_plugin.go
cf install-plugin out/cf-recycle-plugin -f
```
### Download
Binaries are available in the releases section.

### Usage
```sh
cf recycle <APP NAME>
```
