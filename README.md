<h1 align="center">
    <img align="left" width="100" height="100" src="https://zetafence.com/images/logo.png" alt="Zetafence"/>
    <br />
    <p style="color: #808080; text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);">
    Zetafence Cloud Security CLI
    </p>
</h1>

<br/>

## zetacli

Zetafence CLI is a command-line tool to interact with Zetafence management services via API calls.

<br/>

## Obtain zetacli

```
curl -ks https://raw.githubusercontent.com/zetafence/zetacli/main/zetacli \
    -o zetacli
chmod +x zetacli
```

<br />

## General Usage

```
$ ./zetacli -h
usage: zetacli [-h] {set,get,yucca,k8s,aws} ...

Zetafence CLI to interact with management.

positional arguments:
  {set,get,yucca,k8s,aws}
                        Top-level commands
    set                 Set commands
    get                 Get commands
    yucca               Yucca control plane
    k8s                 K8s control plane
    aws                 AWS list security controls

optional arguments:
  -h, --help            show this help message and exit
```

<br/>

## Set Commands

```
$ ./zetacli get -h
usage: zetacli set [-h] [--token TOKEN] [--server SERVER] [--app APP] [--behavior BEHAVIOR]

optional arguments:
  -h, --help           show this help message and exit
  --token TOKEN        Set a token
  --server SERVER      Set Zetafence backend server:port
  --app APP            Set an app
  --behavior BEHAVIOR  Set a behavioral profile
```

<br/>

## Get Commands

```
$ ./zetacli get -h
usage: zetacli get [-h] [--server] [--app] [--behavior]

optional arguments:
  -h, --help  show this help message and exit
  --server    Get Zetafence backend server
  --app       Get the current app
  --behavior  Get the current behavior profile
```

<br/>

## AWS Security Commands

```
$ ./zetacli aws -h
usage: zetacli aws [-h] [--list] [--auth] [--iam] [--exfiltration] [--insiderthreats]
                   [--infravuln] [--privilege] [--monitoring]
                   security

positional arguments:
  security          AWS list info

optional arguments:
  -h, --help        show this help message and exit
  --list            AWS list security info
  --auth            auth and credentials
  --iam             IAM
  --exfiltration    Exfiltration
  --insiderthreats  Insider Threats
  --infravuln       Infra Vulnerabilities
  --privilege       Privilege Escalations
  --monitoring      Monitoring
```

<br/>

## Kubernetes Commands

```
$ ./zetacli k8s -h
usage: zetacli k8s [-h] [--pods] [--deployments] [--service-accounts] [--roles] [--cluster-roles]
                   [--pods-serviceaccounts] [--serviceaccounts-pods] [--deployments-clusterrole]
                   [--clusterrole-roles]
                   list

positional arguments:
  list                  Kubernetes list commands

optional arguments:
  -h, --help            show this help message and exit
  --pods                List pods in Kubernetes
  --deployments         List deployments in Kubernetes
  --service-accounts    List service accounts in Kubernetes
  --roles               List roles in Kubernetes
  --cluster-roles       List cluster roles in Kubernetes
  --pods-serviceaccounts
                        List pods associated with one or more service accounts in Kubernetes
  --serviceaccounts-pods
                        List which service accounts are associated with one or more pods in
                        Kubernetes
  --deployments-clusterrole
                        List which deployments have cluster-role access in Kubernetes
  --clusterrole-roles   List which cluster-role are bound to which roles in Kubernetes
```

<br/>Copyright (C)
    <a href="https://zetafence.com">
    <img align="center" width="85" src="https://img.shields.io/badge/Zetafence-8A2BE2" alt="Zetafence"/></a>2024.
