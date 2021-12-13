# vcluster-on-ocp4

## Install vcluster 

```shell
$ curl -s -L "https://github.com/loft-sh/vcluster/releases/latest" | sed -nE 's!.*"([^"]*vcluster-linux-amd64)".*!https://github.com\1!p' | xargs -n 1 curl -L -o vcluster && chmod +x vcluster;
$ sudo mv vcluster /usr/local/bin;
```

## Create a vcluster

```shell
$ vcluster create vcluster-1 -n host-namespace-1 --extra-values values-k3s.yaml --chart-version v0.5.0-alpha.7
```
