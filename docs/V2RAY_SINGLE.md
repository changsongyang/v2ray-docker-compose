# V2Ray Docker Compose for Single Server

V2Ray is a proxy tool equipped with advanced functionalities and supports protocols such as Shadowsocks, VMess, and Trojan.
Currently, [V2Fly](https://www.v2fly.org) maintains V2Ray.

The simplest and most straightforward method to install V2Ray on a server is by using Docker and Docker Compose,
as outlined in this documentation.

## Setup

To set up V2Ray using Docker Compose, follow the steps outlined below.

1. Install Docker and Docker-compose ([Official Documanetation](https://docs.docker.com/engine/install/#supported-platforms)).
1. Run `git clone https://github.com/miladrahimi/v2ray-docker-compose.git` to download this repository.
1. Run `cd v2ray-docker-compose/v2ray-single-server` to change the directory.
1. Replace `<UPSTREAM-PASSWORD>` in `v2ray.json` with a Shadowsocks password like `FR33DoM`.
1. Run `docker compose up -d`.
1. Run `./clients.py` to generate client configurations.
1. (Optional) Run `./../utils/bbr.sh` to setup BBR and speed up the server network.

## Configuration

The default configuration uses the Shadowsocks protocol, but you can manually add any other protocols supported by V2Ray to the configuration.

For more information about available protocols, refer to the [official documentation](https://www.v2fly.org/v5/config/inbound.html).

## Advanced Solutions

V2Ray on a single server might not work well in highly restricted networks where directly using protocols like Shadowsocks is a struggle.
To set up V2Ray effectively in such environments, check the main documentation in this repository for advanced solutions.

[https://github.com/miladrahimi/v2ray-docker-compose](https://github.com/miladrahimi/v2ray-docker-compose)
