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





예시로 사용하고자 하는 API는

https://tracker.delivery/guide/

위 링크에 있는 것으로

배송추적을 위한 값들이 나열 되어 있는 것이

꽤나 복잡하여서 이것을 예시로 사용하여서

다른 api들은 비교적 더 쉽게 사용이 가능할겁니다.



1. 택배사들 정보

https://apis.tracker.delivery/carriers

2. 배송추적 정보

https://apis.tracker.delivery/carriers/:carrier_id/tracks/:track_id



# Class추가(+@SerializedName)

가장 먼저 위의 api에서 값들을 불러오기 위한 클래스를 새로 만들어 줍니다.

저는 Data.java를 만들어서 사용 했습니다.

일단 택배사 정보를 가져오기 위해

```java
public class Carrier{
    @SerializedName("id") String id;
    @SerializedName("name") String name;
    @SerializedName("tel") String tel;

    public String getId() { return id; }
    public String getName() { return name; }
    public String getTel() { return tel; }
}

public Carrier getCarrier(){ return carrier; }
```



그리고 배송추적 정보를 가져오기 위한

```java
/////////////////Carriers List////////////////////////////////
@SerializedName("id") String id;
@SerializedName("name") String name;
@SerializedName("tel") String tel;

public String getId() { return id; }
public String getName() { return name; }
public String getTel() { return tel; }

/////////////////Tracker////////////////////////////////
////////////////////////////////////////////////////////
@SerializedName("from") From from;
@SerializedName("to") To to;
@SerializedName("state") State state;
@SerializedName("progresses")
public List<Progress> progress = new ArrayList<>();
@SerializedName("carrier") Carrier carrier;

//////////////보내는 사람 정보///////////////////////////////////////
public class From{
    @SerializedName("name") String name;
    @SerializedName("time") String time;

    public String getName() { return name; }
    public String getTime() { return time; }
}
//////////////밥는 사람 정보///////////////////////////////////////
public class To{
    @SerializedName("name") String name;
    @SerializedName("time") String time;

    public String getName() { return name; }
    public String getTime() { return time; }
}
//////////////현재 상태///////////////////////////////////////
public class State{
    @SerializedName("id") String id;
    @SerializedName("text") String text;

    public String getId() { return id; }
    public String getText() { return text; }
}
/////////////진행 상황////////////////////////////////////////
public class Progress{
    @SerializedName("time") String time;
    @SerializedName("location") Location location;
    @SerializedName("status") Status status;
    @SerializedName("description") String description;

    public String getTime() { return time; }
    public String getDescription() { return description; }


    public class Location{//위치-위치의 이름
        @SerializedName("name") String name;

        public String getName() { return name; }
    }
    public class Status{//상태-상태id와 상태(예)배송중
        @SerializedName("id") String id;
        @SerializedName("text") String text;

        public String getId() { return id; }
        public String getText() { return text; }
    }

    public Progress.Location getLocation() {return location;}
    public Progress.Status getStatus() {return status;}

}
/////////////////////////////////////////////////////

public From getFrom(){ return from;}
public To getTo(){ return to;}
public State getState() { return state; }
public List<Progress> getProgress(){ return progress;}
```



## Interface추가

이제 인터페이스를 추가해줘야 합니다.

Retriservice.java 라는 인터페이스를 추가해 줬습니다.

```java
//배송추적 값 가져오기
@GET("/carriers/{track_id}/tracks/{track_number}")
Call<Data> trackingData(@Path("track_id") String track_id, @Path("track_number") String track_number);
//택배사 정보 가져오기
@GET("/carriers")
Call<List<Data>> getCarriers();
```

일단 불러오기 위한 get과 path만을 사용하겠습니다.



## 원하는 값을 Call해서 가져오기

MainActivity에 아래와 같이 추가 해줍니다.

baseurl은 인터페이스에서 전체url을 썼다면 필요없습니다.



```java
String carriername = "kr.epost"; //택배사 이름
String tracknumberedit = "1111111111"; //송장번

//retrofit service 
Retrofit retrofit = new Retrofit.Builder()
        .baseUrl("https://apis.tracker.delivery")
        .addConverterFactory(GsonConverterFactory.create())
        .build();
final Retroservice retroService = retrofit.create(Retroservice.class);
```

baseurl은 인터페이스에서 전체 url을 



그리고 Call해와야 하기 위해서

기본적인 폼을 가져옵니다.



```java
Call<Data> dataP = retroService.trackingData(carriername, tracknumberedit);

dataP.enqueue(new Callback<Data>() {
  
    @Override
    public void onResponse(@NonNull Call<Data> call, @NonNull Response<Data> response) {
        Data user = response.body();
    }
  
    @Override
    public void onFailure(@NonNull Call<Data> call, @NonNull Throwable t) {
        Log.d("TESt", "Failure");
    }
  
});
```

## List로 가져오기(+Adapter)

