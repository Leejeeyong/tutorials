# REST API



Gson Converter가 필요하기 때문에

APP의 build.gradle에서 아래를 추가해줍니다.

```
implementation 'com.squareup.retrofit2:retrofit:2.6.0'
implementation 'com.squareup.retrofit2:converter-gson:2.6.0'
```

그리고 인터넷 권한을 허용해주기 위해

AndroidManifest.xml 에서 아래를 앱속성을 다루기 전의 부분에 추가해줍니다.

```
<uses-permission android:name="android.permission.INTERNET" />
```





## Interface추가

## Class추가(+@SerializedName)

## 원하는 값을 Call해서 가져오기

## List로 가져오기(+Adapter)