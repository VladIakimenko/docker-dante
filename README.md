# Dante & Docker

Dante is a free SOCKS server and a SOCKS client, implementing RFC 1928 and
related standards. 

## Software specficiation

* Base image: Alpine Linux
* Dante version: 1.4.2
* [![](https://images.microbadger.com/badges/image/adegtyarev/dante.svg)](https://microbadger.com/images/adegtyarev/dante "the download size and the number of layers")

## Usage

The image is ready to run Dante server or client in a Docker environment:

    $ docker run --rm adegtyarev/dante sockd -v
    Dante v1.4.2.  Copyright (c) 1997 - 2014 Inferno Nettverk A/S, Norway

Set the following parameters:

* *SOCKD_USER_NAME*: the username to use by clients
* *SOCKD_USER_PASSWORD*: the password to use by clients

The SOCKS server should be up and ready to serve.  An example command to test
the proxy service you have just set up:

    $ curl -x socks5h://username:password@127.0.0.1:1080 http://example.com

## Author

Alexey Degtyarev @adegtyarev
