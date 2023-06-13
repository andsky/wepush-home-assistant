# wepush-home-assistant
home assistant 实现微信通知


## 申请 token
https://wepush.wanyoukeji.com/ 




## 在 Configuration.yaml 文件中添加以下配置，用于配置 notify 并指向 wepush

```
notify:
  - name: wepush
    platform: rest
    resource: https://wepush.wanyoukeji.com/v1/api/push
    method: POST
    message_param_name: text
    data:
      token: YOUR_TOKEN_HERE
```

## 使用
调用  notify.wepush 发送信息
