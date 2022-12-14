# Description
Simple endpoints monitoring solution with Prometheus, blackbox exporter and alertmanager with telegram for alerts.

# What to do
Copy this repository to your desired host with git clone 
```
git clone git@github.com:jafnhaar/docker-compose-blackbox.git
cd docker-compose-blackbox
```
Next you have to make some changes to the provided config files:
### alertmanager
```
vim alertmanager/config.yml
```
Change bot_token to your bot token (can be optained via @botfather bot in telegram) and enter desired chat_id.
### prometheus
```
vim prometheus/prometheus.yml
```
Change static targets configs to your desired hosts. There currently http and icmp probes implemented.
### bringing everything up
```
docker-compose up -d
```
Everything should be working fine from now. You can check web interface of prometheus at <your_ip_address:9090>, alertmanager at <your_ip_address:9093> and blackbox exporter at <your_ip_address:9115>
