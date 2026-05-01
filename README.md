## Задание 1

Вам необходимо поднять в докере и связать между собой:

- elasticsearch (hot и warm ноды);
- logstash;
- kibana;
- filebeat.  

![](./pictures/Pasted%20image%2020260501183718.png)  

---

![](./pictures/Pasted%20image%2020260501184127.png)  
![](./pictures/Pasted%20image%2020260501184209.png)  

---

### 🔥 es-hot
node.roles=master,data_content,data_hot 

- принимает новые данные
- активно индексирует
- быстрый доступ

---

### 🧊 es-warm
  
node.roles=master,data_warm  

- хранит старые данные    

---

### Kibana интерфейс

![](./pictures/Pasted%20image%2020260501185059.png)  

---

## Задание 2

Для того чтобы можно было искать по данным создаю Index-patterns  

![](./pictures/Pasted%20image%2020260501191139.png)  

---

### Почему logstash а не filebeat?

В проекте схема такая:  
Filebeat → Logstash → Elasticsearch  

filebeat НЕ пишет напрямую в Elasticsearch  

![](./pictures/Pasted%20image%2020260501191357.png)  
![](./pictures/Pasted%20image%2020260501191439.png)  

---

### Проверка генерации логов

Убеждаюсь что приложение генерирует логи   

![](./pictures/Pasted%20image%2020260501192027.png)  

---

### Проверка индексов в Elasticsearch

Проверяем факт существования данных в кластере    

![](./pictures/Pasted%20image%2020260501192333.png)  
![](./pictures/Pasted%20image%2020260501193118.png)  
![](./pictures/Pasted%20image%2020260501193225.png)  
![](./pictures/Pasted%20image%2020260501193318.png)    
