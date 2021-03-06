### 发布Android程序生成APK
#### [一、命令行生成方式]()
```
keytool -genkey -alias android123.keystore -keyalg RSA -validity 20000 -keystore android123.keystore
```
![image](https://github.com/ningbaoqi/AndroidSecurityAndRelease/blob/master/gif/pic1.jpg)

+ `-validity`表示证书有效天数；

![image](https://github.com/ningbaoqi/AndroidSecurityAndRelease/blob/master/gif/pic2..jpg)

+ 双击`Gradle->项目：app下的assemble`，然后在`build->outputs->apk->release`就可以找到未签名的`apkapp-release-unsigned.apk`;

```
jarsigner -verbose -keystore android123.keystore -signedjar android123_signed.apk app-release-unsigned.apk android123.keystore
```

![image](https://github.com/ningbaoqi/AndroidSecurityAndRelease/blob/master/gif/pic3.jpg)

#### [二、使用AndroidStudio生成方式]()

```
Build->Generate Signed APK...//然后根据提示就可以生成APK了
```
![image](https://github.com/ningbaoqi/AndroidSecurityAndRelease/blob/master/gif/pic10.jpg)
![image](https://github.com/ningbaoqi/AndroidSecurityAndRelease/blob/master/gif/pic11.jpg)

#### [三、使用Gradle生成方式](https://github.com/ningbaoqi/AndroidSecurityAndRelease/commit/4d959be2ae09093426ce85e1d5237d63e73aaffb)

![image](https://github.com/ningbaoqi/AndroidSecurityAndRelease/blob/master/gif/pic15.jpg)
