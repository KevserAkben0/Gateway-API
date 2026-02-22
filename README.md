# API Gateway

## 1. API Gateway Nedir?

API Gateway, istemciler ile backend servisleri arasında çalışan ve tüm API trafiğini yöneten merkezi bir katmandır.

Microservice mimarisinde her servis ayrı çalışır.  
Client’ın her servise ayrı bağlanması yerine API Gateway kullanılır.

Cloud-native mimarilerde API Gateway, güvenlik ve trafik kontrolünün merkezi noktasıdır.

---

## 2. API Gateway Nasıl Çalışır?

1. Client isteği Gateway’e gönderir  
2. Gateway isteği doğrular  
3. İsteği uygun backend servise yönlendirir  
4. Response alıp client’a döner  

Gateway şu işlemleri yapabilir:

- Authentication / Authorization
- Rate limiting
- Logging
- Monitoring
- Routing
- Load balancing

---

## 3. API Gateway Neden Kullanılır?

- Merkezi güvenlik sağlar  
- Observability (log, metrics, tracing) sağlar  
- Client tasarımını basitleştirir  
- Performansı artırabilir  

---

## 4. Dezavantajları

- Tek hata noktası olabilir  
- Yanlış tasarım bottleneck yaratabilir  
- Fazla logic eklenirse monolith’e dönüşebilir  

---

# 5. Popüler API Gateway Araçları

## 5.1 Envoy

- L7 proxy olarak çalışan data-plane bileşenidir  
- HTTP/gRPC trafiğini alır  
- Route kurallarına göre yönlendirir  
- Filter chain ile auth, rate limit ve telemetry uygular  

---

## 5.2 Kong

- Temelinde NGINX vardır  
- Lua tabanlı plugin sistemi kullanır  

---

## 5.3 Apache APISIX

- NGINX tabanlıdır  
- Dynamic configuration kullanır  
- Config değişince restart gerekmez  
- etcd üzerinden runtime config alır  

---

## 5.4 KrakenD

- Tamamen stateless çalışır  
- API Aggregation özelliği vardır  

👉 Tek request → birden fazla backend çağrısı → tek response

---

## 5.5 Tyk

- API lifecycle platformudur  
- Gateway + Dashboard + Analytics içerir  

---

## 5.6 Traefik

- Event-driven çalışır  
- Docker/Kubernetes’te yeni servis açıldığında otomatik route oluşturur  

---

## 5.7 NGINX API Gateway

- Reverse proxy mantığıyla çalışır  
- Worker process modeli  
- Event-driven I/O  

---

## 5.8 Ambassador / Emissary

- Envoy üzerine kuruludur  
- Kubernetes CRD kullanır  

---

## 5.9 Gloo Edge

- Envoy üzerine control layer ekler  
- API discovery  
- GraphQL federation  
- Serverless routing  

---

## 5.10 Gravitee.io

- Event-driven gateway  
- Streaming API’ler için optimize edilmiştir  

---

# Sonuç

API Gateway, microservice mimarisinde güvenlik, trafik yönetimi ve servisler arası iletişimi kolaylaştıran kritik bir bileşendir.

Doğru tasarlandığında sistem performansını artırır ve yönetimi kolaylaştırır.
