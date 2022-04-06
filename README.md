# Kafka Cluster

## 목적
**임의로 생성되는 데이터에 대해 이상데이터를 찾아 Postgresql 내 쌓는 kafka pub/sub cluster 구축**

![image](https://user-images.githubusercontent.com/79136484/161947387-7a07ac3f-637c-4e9f-b982-cdd9d6915e25.png)



 
# 알게된 것 
* Kafka
* Docker compose
* Kafdrop
* Python을 이용한 Kafka 프로그래밍

 
## Repository 구조
```
.
├── docker-compose.yml      # docker-composer YAML 파일
├── payment_producer.py     # 결제 방식 데이터 랜덤 생성 Producer
├── fraud_detector.py       # 결제 방식 데이터를 구독해 'bitcoin'에 해당하는 데이터와 아닌 데이터 구분해서 produce
├── fraud_processor.py      # 'bitcoin'에 해당하는 데이터 구독 및 postgreSql insert
├── legit_processor.py      # 'bitcoin'에 해당하지 않는 데이터 구독 및 postgreSql insert
└── README.md
 
```
