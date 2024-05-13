# Split-Akvorado-into-3-VM
## Part I: Install Kafka
- Step 1: Install Java 
```
sudo apt update
```
```
sudo apt install default-jre
```
- Step 2: Install Kafka
```
wget https://www.apache.org/dyn/closer.cgi?path=/kafka/3.7.0/kafka_2.13-3.7.0.tgz
```
```
tar -xzf kafka_2.13-3.7.0.tgz
cd kafka_2.13-3.7.0
```
```
sudo mv kafka_*/ /usr/local/kafka
```
```
sudo chown kafka:kafka -R /usr/local/kafka
```
```
sudo mkdir /usr/local/kafka/tmp/zookeeper
```
```
sudo chown kafka:kafka -R /usr/local/kafka
```
```
sudo nano /usr/local/kafka/config/zookeeper.properties
```
Change this line<br>
```
dataDir=/usr/local/kafka/tmp/zookeeper
```
```
sudo nano /usr/local/kafka/config/server.properties
```
Change this line<br>
```
log.dirs=/usr/local/kafka/kafka-logs
```
## Part III: Install Akvorado
- Step 1: Install Akvorado
```
wget https://github.com/akvorado/akvorado/releases/download/v1.10.1/akvorado
```
- Step 2: Config Akvorado
```
chmod +x akvorado
```
Create a user for Akvorado<br>
```
sudo useradd -r -s /bin/false akvorado

```
```
sudo mv akvorado_ac /etc/bash_completion.d/akvorado
```
```
nano /etc/akvorado.yaml
```
 sudo chown akvorado:akvorado /etc/akvorado.yaml
```
sudo mkdir /var/lib/akvorado
sudo mkdir /usr/share/GeoIP
```
```
wget https://share.walrustech.org/GeoLite2-ASN.mmdb
```
```
sudo mv GeoLite2-ASN.mmdb /usr/share/GeoIP/GeoLite2-ASN.mmdb
```
```
sudo chown -R akvorado:akvorado /usr/share/GeoIP/
```





