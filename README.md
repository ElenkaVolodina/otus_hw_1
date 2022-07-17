## Основы работы с Kubernetes

### Домашняя работа № 1

### Используемый Docker образ
```shell
docker pull elenkavolodina/otus_hw_1_fast_api:latest
```

### Запуск приложения
```shell
cd k8s
kubectl create namespace otus-hw-1-volodina
kubectl apply -f .
```
### Удаление приложения
```shell
kubectl delete namespaces otus-hw-1-volodina
```

### Postman коллекция
```shell
newman run postman_collection/otus_hw_1.postman_collection.json
```
          
```shell
newman

otus_hw_1

→ Get health
  GET http://arch.homework/health [200 OK, 147B, 69ms]
  ✓  Test status 200
  ✓  Test content

→ Get with rewrite
  GET http://arch.homework/otusapp/elena [200 OK, 147B, 15ms]
  ✓  Test rewrite

→ Get 404
  GET http://arch.homework/health/otusapp_new/elena [404 Not Found, 161B, 5ms]
  ✓  Test 404

┌─────────────────────────┬──────────────────┬──────────────────┐
│                         │         executed │           failed │
├─────────────────────────┼──────────────────┼──────────────────┤
│              iterations │                1 │                0 │
├─────────────────────────┼──────────────────┼──────────────────┤
│                requests │                3 │                0 │
├─────────────────────────┼──────────────────┼──────────────────┤
│            test-scripts │                6 │                0 │
├─────────────────────────┼──────────────────┼──────────────────┤
│      prerequest-scripts │                3 │                0 │
├─────────────────────────┼──────────────────┼──────────────────┤
│              assertions │                4 │                0 │
├─────────────────────────┴──────────────────┴──────────────────┤
│ total run duration: 194ms                                     │
├───────────────────────────────────────────────────────────────┤
│ total data received: 52B (approx)                             │
├───────────────────────────────────────────────────────────────┤
│ average response time: 29ms [min: 5ms, max: 69ms, s.d.: 28ms] │
└───────────────────────────────────────────────────────────────┘

```
