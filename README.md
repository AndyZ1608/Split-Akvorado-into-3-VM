### Split-Akvorado-into-3-VM
Part I: Install Kafka
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
