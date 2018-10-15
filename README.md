### Prometheus stack


1. Add the following to enable docker daemon to expose its metrics

```bash
$ cat /etc/docker/daemon.json

{
    "metrics-addr" : "0.0.0.0:9323",
    "experimental" : true
}
```

2. Clone the repo

```bash
$ git clone git@github.com:shreben/prometheus.git
```

3. Enter the directory and run the stack

```bash
$ cd prometheus/
$ docker-compose up -d
```

4. Locate the tools under the following URLs

	- http://localhost:3000		grafana (admin/foobar)
	- http://localhost:9090		prometheus
	- http://localhost:9093		alertmanager
	- http://localhost:8500/ui/ consul
	- http://localhost:8080		cadvisor
