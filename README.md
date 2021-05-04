# tencent-cloud-cos-upload-image

原版：https://github.com/Galen-Yip/tencent-cloud-cos-upload-image

对原版进行一些修改

## 使用

`cmd + opt + o` 选择本地文件上传至 COS

## 发布

```sh
npm run deploy
```

## 参数配置

```js
{
    // 地区，在COS对象存储中bucket对应的地域
    "tencentCOSUpload.region": "",
    // secretId，在 https://console.cloud.tencent.com/cam/capi 中获取
    "tencentCOSUpload.secretId": "",
    // secretKey，在 https://console.cloud.tencent.com/cam/capi 中获取
    "tencentCOSUpload.secretKey": "",
    // 输入你的bucket名称，如 a-1250000000
    "tencentCOSUpload.bucket": "",
    // remotePath，您的存储目录，例如要把文件存在 http://${你的域名}/images/png 这个目录下，则这里填写images/png。默认为空，即存储在根路径下
    "tencentCOSUpload.remotePath": "",
    // 存储桶是否为公有可访问，如为私有，且希望上传后的url带签名，则设置为false，默认是 true
    "tencentCOSUpload.isPublic": "true",
    // 签名有效期，单位为妙，isPublic设置为 false 时有效
    "tencentCOSUpload.duration": "31536000",
    // 自定义域名，原来替换引用的默认COS域名，无特殊需求可不用修改
    "tencentCOSUpload.domain": "",
    // 临时目录，默认 /tmp/.tencentCOSUpload，无特殊需求可不用修改
    "tencentCOSUpload.localPath": "/tmp/.tencentCOSUpload"
}
```
