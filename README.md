# ELK Stack Project

What is the ELK Stack?

The ELK Stack is a collection of three open-source products — Elasticsearch, Logstash, and Kibana. 

ELK stack provides centralized logging in order to identify problems with servers or applications. It allows you to search all the logs in a single place. It also helps to find issues in multiple servers by connecting logs during a specific time frame.

- E stands for ElasticSearch: used for storing logs
- L stands for LogStash: used for both shipping as well as processing and storing logs
- K stands for Kibana: is a visualization tool (a web interface) which is hosted through Nginx or Apache
ElasticSearch, LogStash and Kibana are all developed, managed ,and maintained by the company named Elastic.

ELK Stack is designed to allow users to take data from any source, in any format, and to search, analyze, and visualize that data in real time.

![ELK STACK](./images/ELK%20Stack.png)

ELK Stack Architecture

- Logs: Server logs that need to be analyzed are identified
- Logstash: Collect logs and events data. It even parses and transforms data
- ElasticSearch: The transformed data from Logstash is Store, Search, and indexed.
- Kibana: Kibana uses Elasticsearch DB to Explore, Visualize, and Share

For this project we have created an infrastructure consisting of 3 ELK servers and a server called Beats, which sends dummy logs to the Logstash server, which are then processed by Elasticsearch and displayed via the web by Kibana.

Each server is automatically configured using Ansible, a tool that allows you to manage the configuration and installation of applications on each server through specific instructions (called playbook).

All this is made even more automatic thanks to Github Actions, which allows you to test the code we uploaded to the repository and finally deploy it on the server, if the test is successful.

More info about [ELK](https://aws.amazon.com/opensearch-service/the-elk-stack/#:~:text=What%20is%20the%20ELK%20stack,Elasticsearch%2C%20Logstash%2C%20and%20Kibana.).