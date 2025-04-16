steps that the services follow

step0
pre-requesites and requirements
step1
installation and setup
step2 
configuration and networking
step3 
api's (commands) and development
step 4
hardening/patching and observability

# highlevel overview 
## example:
## step0
4gb ram
2 cpu
arm or amd architecture

step1
elasticsearch installation commands:
   39  apt-get update && sudo apt-get install -y apt-transport-https
   40  sudo apt-get install -y default-jre
   41  wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo gpg --dearmor -o /usr/share/keyrings/elasticsearch-keyring.gpg
   42  echo "deb [signed-by=/usr/share/keyrings/elasticsearch-keyring.gpg] https://artifacts.elastic.co/packages/8.x/apt stable main" | sudo tee /etc/apt/sources.list.d/elastic-8.x.list
   43  sudo apt-get update
   44  sudo apt-get install -y elasticsearch
   45  sudo systemctl daemon-reload && sudo systemctl enable elasticsearch.service && sudo systemctl start elasticsearch.service
   46  sudo systemctl status elasticsearch
   47  ifconfig
   48  curl -k -u elastic:u5cK5fPbgwed7Bdkvdvk https://localhost:9200
   49  sudo systemctl enable elasticsearch

step2
### this directory have all the configuration
/etc/elasticsearch/
root@ubuntu-linux-2404:~# ls /etc/elasticsearch/
certs                   elasticsearch-plugins.example.yml  jvm.options    log4j2.properties  roles.yml  users_roles
elasticsearch.keystore  elasticsearch.yml                  jvm.options.d  role_mapping.yml   users

### elasticsearch.yml file is the main configuration for the elasticsearch agent, configuring xpack and ssl/tls

## step2
### this this location have a elastic related binaries and we use certutils to generate ca and certificate crt and key
root@ubuntu-linux-2404:~# cd /usr/share/elasticsearch/bin/
root@ubuntu-linux-2404:/usr/share/elasticsearch/bin# ls
elasticsearch                          elasticsearch-env            elasticsearch-reconfigure-node  elasticsearch-sql-cli
elasticsearch-certgen                  elasticsearch-env-from-file  elasticsearch-reset-password    elasticsearch-sql-cli-8.18.0.jar
elasticsearch-certutil                 elasticsearch-geoip          elasticsearch-saml-metadata     elasticsearch-syskeygen
elasticsearch-cli                      elasticsearch-keystore       elasticsearch-service-tokens    elasticsearch-users
elasticsearch-create-enrollment-token  elasticsearch-node           elasticsearch-setup-passwords   systemd-entrypoint
elasticsearch-croneval                 elasticsearch-plugin         elasticsearch-shard
root@ubuntu-linux-2404:/usr/share/elasticsearch/bin# 
root@ubuntu-linux-2404:~# ls /etc/elasticsearch/

## step3 
### you might have different ways of interacting with the program or service
root@ubuntu-linux-2404:~# curl -X GET -k "https://localhost:9200" -u elastic:password
{
  "name" : "ubuntu-linux-2404",
  "cluster_name" : "elasticsearch",
  "cluster_uuid" : "-uRcsRVQT2WjJdn66nCsrQ",
  "version" : {
    "number" : "8.18.0",
    "build_flavor" : "default",
    "build_type" : "deb",
    "build_hash" : "04e979aa50b657bebd4a0937389308de82c2bdad",
    "build_date" : "2025-04-10T10:09:16.444104780Z",
    "build_snapshot" : false,
    "lucene_version" : "9.12.1",
    "minimum_wire_compatibility_version" : "7.17.0",
    "minimum_index_compatibility_version" : "7.0.0"
  },
  "tagline" : "You Know, for Search"
}
root@ubuntu-linux-2404:~# 

## step 4
###
apt update elasticsearch 
