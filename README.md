# fritzbox

Expose and access Prometheus metrics for your FRITZ!Box and visualize them with Grafana.

## Introduction

Utilizes Docker images via `docker-compose`:

- [`pdreker/fritz_exporter`](https://hub.docker.com/r/pdreker/fritz_exporter)
- [`prom/prometheus`](https://hub.docker.com/r/prom/prometheus)
- [`grafana/grafana`](https://hub.docker.com/r/grafana/grafana)

**Warning:** No explicit data persistence.

## Setup

- [Create a new FRITZ!Box user](http://fritz.box/?lp=mUser) with appropriate rights. 
- Copy `.env.dist` to `.env` and adjust accordingly.

## Environment


| env            | default     | description              |
|----------------|-------------|--------------------------|
| `FRITZ_HOST`   | `fritz.box` | FRITZ!Box hostname       |
| `FRITZ_USER`   | `fritz`     | FRITZ!Box username       |
| `FRITZ_PASS`   | -           | FRITZ!Box password       |
| `GRAFANA_USER` | `fritz`     | Grafana (admin) username |
| `GRAFANA_PASS` | -           | Grafana (admin) password |

## Start

Run `docker-compose up` & open your browser under [`http://localhost:3000/d/fritz`](http://localhost:3000/d/fritz).

## Stop

Discard with `docker-compose down`

