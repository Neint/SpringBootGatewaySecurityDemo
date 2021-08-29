## 来源：securitydemo（在作者的基础上优化了pom.xml工程结构）
https://www.bilibili.com/read/cv7590217

## 准备工作
### 增加 Redis key
```text
redis-cli -h 10.0.191.10 -p 6379 -a amdyes
set 67f9b705-987b-4534-854e-544f8ca733a6 "{'uri': 'http://localhost:8082/test/test', 'clazz': 'com.example.repserver.bean.dto.TestDto'}"
```
### 检查是否添加成功
```text
get 67f9b705-987b-4534-854e-544f8ca733a6
```

## 打开postman测试
```text
http://localhost:8080/test/test
如果控制台显示如下结果，则测试成功
`{"applyMsg":"申请成功，请保管好个人","applyCode":"288700","applyStatus":"500"}`
```