# 安裝 Rancher

## 官方文件

[Rancher official doc](https://rancher.com/docs/rancher/v2.x/en/quick-start-guide/deployment/quickstart-manual-setup/)

## Step1. 安裝 Docker

## Step2. 安裝 Rancher

```bash
docker run -d --restart=unless-stopped \
  -p 80:80 -p 443:443 \
  rancher/rancher:latest
```

## Step3. 連到 Rancher 介面

以打開瀏覽器，輸入安裝 Rancher 主機的 ip，照著流程即可......\(設定密碼、域名....\)

## Step4. 完成

登入成功即可看到以下畫面

![](.gitbook/assets/1%20%284%29.PNG)



