### 发布Android程序生成APK
#### 生成签名文件
##### 一、命令行生成方式
```
keytool -genkey -alias android123.keystore -keyalg RSA -validity 20000 -keystore android123.keystore
```
