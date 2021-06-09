# liferay-elasticsearch

Depend on the liferay version and set up

- Elasticsearch 7.x

**Step 1 — Installing and Configuring Elasticsearch**
+ curl -fsSL https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -
+ echo "deb https://artifacts.elastic.co/packages/7.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-7.x.list
+ sudo apt update
+ sudo apt install elasticsearch

**Step 2 — Configuring Elasticsearch**
+ sudo nano /etc/elasticsearch/elasticsearch.yml

![image](https://user-images.githubusercontent.com/73691210/121324881-574f4b80-c93b-11eb-8de7-cc268a8b017d.png)

+ sudo systemctl start elasticsearch
+ sudo systemctl enable elasticsearch

**Step 3 — Securing Elasticsearch**
+ sudo ufw allow from 198.51.100.0 to any port 9200
+ sudo ufw enable
+ sudo ufw status

- Step 4 — Testing Elasticsearch
+ curl -X GET 'http://localhost:9200'
