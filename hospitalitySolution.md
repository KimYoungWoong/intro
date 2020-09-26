#Guest Portal
- Frontend : Vue.js, Nuxt,js, SCSS
- Backend  : Node.js, Hapi
- 데이터베이스: Mysql
- 참여율 : 100%


    숙소 예약고객에게 숙소정보가 제공되는 B2C 서비스.
    Frontend
    - Vue.js 로 시작했으나, 1차 버전 업로드 후 Nuxt.js 로 전환.
    Backend 
    - Mashup API 에는 CSRF 적용하여 Proxy Server 를 구성하였고,
    - Service API 에서는 Database Connection 과 user token 을 redis 로 관리하였고, 외부 정보는 KMS를 활용해 데이터 암호화 진행
# In Room Control
- Frontend : Nuxt.js
- 참여율 : 100%


    Guest Portal 내 객실제어 서비스.
    Frontend 에서 Appsync 와 socket 으로 연결하여 객실 제어
# KT Gigagenie Web Application
- Frontend : HTML, Javascript
- Backend : Node.js
- 참여율 : 100%


    KT Gigagenie 의 Dialog Kit 을 활용하여 객실 음성제어 서비스 제공.
    Serverless 로 구성하였으며, API Gateway 와 Lambda 로 HTML Page 와, Restful API 구성
# IoT Hub
- Backend : Node.js
- 참여율 : 100%


    Raspberry PI 를 객실 통신시설과 연결하여 객실정보를 캐치하고(Serial 통신), 캐치한 데이터를 IoT 로 전송하여,
    Cloud 환경에서 객실에 대한 정보를 제공.
    
# Room Management System
- Backend : Node.js
- 참여율 : 40%


    Serverless 로 구성하였으며, API Gateway 와 Lambda 로 Restful API 구성
    Kinesis 를 통해 Queue 를 구성하고, 객실 데이터를 IoT 로 MQTT 통신
