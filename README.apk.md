### 发布Android程序生成APK
#### 生成签名文件
##### 一、命令行生成方式
```
keytool -genkey -alias android123.keystore -keyalg RSA -validity 20000 -keystore android123.keystore
```
![image](https://github.com/ningbaoqi/AndroidSecurityAndRelease/blob/master/gif/pic1.jpg)

+ `-validity`表示证书有效天数；

![image](https://github.com/ningbaoqi/AndroidSecurityAndRelease/blob/master/gif/pic2.jpg)

+ 双击`Gradle->项目：app下的assemble`，然后在`build->outputs->apk->release`就可以找到未签名的`apkapp-release-unsigned.apk`;

```
jarsigner -verbose -keystore android123.keystore -signedjar android123_signed.apk android123.apk android123.keystore
```
