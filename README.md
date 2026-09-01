# Deprecated
Check this repository instead: [Service Status Indicator](https://github.com/Ujjwalkr0001/ServiceStatus)

Or the site: [Site](https://service-status-indicator.remiservices.uk/) 

## Service Status Indicator API

## Description

The Service Status Indicator API is a part of the Server Status Indicator. It provides the essential data for the Server Status Indicator, which is a tool for monitoring the status of various services and system updates on a Linux server. The API comes with some predefined check scripts for common use cases like system updates and services status checking. It can also easily expand its functionality, allowing you to create and add your own custom service checker along with a custom script.

## Target Audience

The Service Status Indicator API targets Linux users who want to have an eye on some services on some system. While it is primarily designed for server use, it can be used locally as well.

## Installation

To install the Service Status Indicator API, you will need to have Python 3 installed on the Linux system, as well as the `flask` and `gunicorn` Python packages. You can install these packages using pip:

```shell
pip install flask gunicorn
```

Once you have installed the required dependencies, you can clone this repository and run the install.sh script as sudo:

```shell
git clone https://github.com/Ujjwalkr0001/ServiceStatus.git
cd ServiceStatus
sudo ./install.sh
```

Note: You will need the authentication `token` to access the API.

After running the `install.sh` script, you can access the API by navigating to http://localhost:8000/services in your web browser and parsing the `authentication header`. If you are running the Service Status Indicator API on a remote server, replace `localhost` with the IP address or domain name of the server.

Note: The Service Status Indicator is currently only supported on Linux.

## Usage

This API is designed to be used as a backend for the front-end client, which is a system indicator that displays the status of various services of a Linux system. The Service Status Indicator API runs as a system service with Gunicorn, which is a WSGI HTTP Server.

Once the server is running, you can access the API by sending HTTP authenticated requests to http://localhost:8000/services. You can use a tool like `curl` or `Postman` to send requests to the API.

```
curl -H 'AUTHORIZATION: Token <Your-Token>' http://localhost:8000/services
```

Response:

```json
{ "System Updates": "ok" }
```

## Gnome extension demo

![service-status-indicator-gnome-extension-demo](demo/service-status-indicator-demo.gif)

## Contributing

If you would like to contribute to the Service Status Indicator API, please read the [CONTRIBUTING.md](CONTRIBUTING.md) file for guidelines on how to contribute to the project.

## Credits

The Service Status Indicator API was created by Ujjwal Kumar and is licensed under the GPLv2 license.


