# PASS
Vue (NuxtJS), NodeJS (Hapi), Mysql, Typescript (NestJS)
### 숙소 예약고객에게 숙소정보 및 객실 IoT 를 제공하는 B2C 서비스.
FE
```
Vue 로 시작하여, 리뉴얼을 통해 NuxtJS 로 전환.
페이지를 레이어로 구성하여, 원페이지 형태의 웹페이지를 제공.
재활용이 가능한 컴포넌트를 구분하고 해당 컴포넌트를 레이어에 적용하는 형태로 개발.
```
BE
```
보안을 위해 외부에서 접근이 가능한 External API 와, External API 에서만 접근을 허용한 Service API 로 구성.
External API 에서는 외부에서 접근이 가능하기 때문에 XSS, CSRF 등 공격에 대비하여 구성.
Service API 는 DB 와 직접 연결하며, 서비스를 구성하기 위한 정보를 제공하고, User 관리를 위해 Redis 로 User Token 을 구성.
-
External API 의 역할이 Proxy 외에 특별한 역할이 없어, Mashup API 로 변경하여 정보를 취합해서 필요한 정보만 전달할 수 있도록 변경
변경된 Mashup API 는 Typescript (NestJS) 로 구축.
```

# KT Gigagenie Web Application
Nodejs (Hapi)
### KT Gigagenie 의 Dialog Kit 을 활용하여 객실 음성제어 서비스 제공.
```
Serverless 형태로 구축하기위해 APIGateway 와 Lambda 로 외부 페이지와 Restful API 구현
Web Application 을 사용하지 않기로 하여, 서비스 종료
```
# IoT Hub
Nodejs (Hapi)
### 클라우드 환경에서 객실 정보를 확인하기 위한 HUB
```
하드웨어는 RaspberryPI 를 사용하고, RaspberryPI 내에 NodeJS 로 작성
객실 데이터를 SerialPort 를 통해 통신 데이터를 캐치하고, 해당 객실 데이터를 가공하여 MQTT 통신으로 AWS IoT 로 전송
``` 
# Room Management System
NodeJS (Hapi), Mysql, Typescript (NestJS)
### 숙소 내 객실 관리 시스템
```
Serverless 로 구성하였으며, API Gateway 와 Lambda 로 Restful API 구성
Kinesis 를 통해 Queue 를 구성하고, 객실 데이터를 IoT 로 MQTT 통신
-
리펙토링을 통해 Serverless 형태를 없애고, NodeJS (Hapi) 로 구성
모든 데이터를 하나의 서버에서 관리하며, 각 서버는 데이터 서버에서 데이터를 제공받아 서비스를 제공하는 형태로 변경
일부 서비스를 Typescript (NestJS) 로 변경
```
