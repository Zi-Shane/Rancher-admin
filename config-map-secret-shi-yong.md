# Config Map & Secret 使用

#### configmap 是用來儲存設定檔案的 volume，例如 nginx 的設定檔

#### secret 是用來儲存機密資料，像是 ip, mysql\_passowrd....

兩者都可以以 Volume 或 ENV 的方式傳入 Pod

## Step1. 新增 Config Map, Secret

到 Cluster -&gt; Peoject -&gt; Resources -&gt; ConfigMap\(Secret\)，按 Add Config Map\(Secret\) ，新增一個 ConfigMap\(Secret\)

## Step2. 設定 Value

![](.gitbook/assets/1%20%287%29.PNG)

## Step3-1. 傳入 Pod \(以 Volume\)

到 Application 掛載到 Volume

![](.gitbook/assets/4%20%282%29.PNG)

可以在掛載目錄下，找到 nginx.conf

![](.gitbook/assets/3%20%283%29.PNG)

## Step3-2. 傳入 Pod \(以 ENV\)

到 Environment Variables 選下方 Add From Source

Type 可以選 ConfigMap or Secret

![](.gitbook/assets/4%20%285%29.PNG)

Container 內可以找到設定的 secret

![](.gitbook/assets/5%20%283%29.PNG)

