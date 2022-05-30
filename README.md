# ELK(Docker) via Ansible

Simple utility to deploy ELK-Stack and Filebeat in docker containers \
Used technologies:
- Ansible
- Docker, Docker-Compose
- Elasticsearch, Logstash, Kibana, Filebeat

## Project Structure


```
ansible-elk
├── docker
│   ├── defaults
│   │   └── main.yml
│   ├── handlers
│   │   └── main.yml
│   ├── tasks
│   │   ├── docker-compose.yml
│   │   ├── docker-https.yml
│   │   ├── main.yml
│   │   └── pip-install.yml
│   └── vars
│       └── main.yml
├── docker-compose.yml
├── elk
│   ├── elasticsearch
│   │   ├── files
│   │   │   ├── config
│   │   │   │   └── elasticsearch.yml
│   │   │   └── Dockerfile
│   │   └── tasks
│   ├── kibana
│   │   └── files
│   │       └── Dockerfile
│   ├── logstash
│   │   ├── files
│   │   │   └── Dockerfile
│   │   └── pipeline
│   │       └── logstash.conf
│   └── tasks
│       └── main.yml
├── hosts
├── logstash
│   └── pipeline
├── README.md
└── start.yml
```

## Installation

Requires [Ansible](https://www.ansible.com/) to run.

Clone repository to your machine and check inventory file

```sh
git clone https://gitlab.wltm.ru/vjacheslav.gordienko/ansible-elk.git
cd ansible-elk
ansible-inventory -i ./hosts --list
```


