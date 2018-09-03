# 資源限制

## Resource limit

### 資源種類

* CPU
* Memory 

### 基本單位

* 1 個 cpu \(Hyperthread\)
  * 100m\(millicpu\) = 0.1 unit of cpu
* 1 bytes 
  * 500 Mi 
  * 10 Gi

### 限制型態以 container 為單位作限制

* spec.containers\[\].resources.limits.cpu
* spec.containers\[\].resources.limits.memory
* spec.containers\[\].resources.requests.cpu
* spec.containers\[\].resources.requests.memory

#### limits: 限制最高, requests: 保證最低

### 規則

`0 <= request <= Node Allocatable`

 `request` &lt;= `limit` &lt;= Infinity

## 在 Rancher 上設定

任一個 Application 底下，找到 Security & Host Config 下半部有 CPU, Memory Reservation 可以限制使用資源

![](.gitbook/assets/image%20%287%29.png)

