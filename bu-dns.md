# Pod 之間溝通

## 透過 pod name 可以解析到 pod ip \(ping 到其他 pod\)

在同一個 namespace 底下，可以用 `ping <pod-name>` 指令 ping 到同一個 namespace 底下的 pod

在不同 namespace 底下， 可以用 `ping <pod-name>.<namespace>` 指令 ping 到其他 &lt;namespace&gt; 下的   pod

![](.gitbook/assets/image%20%284%29.png)

在 namespace02 底下， busybox 可以用 `ping nginx` 指令 ping 到 nginx pod

在 namespace02 底下， busybox 可以用 `ping ubuntu.default` 指令 ping 到 default 下的  Ubuntu pod

![](.gitbook/assets/image%20%282%29.png)

