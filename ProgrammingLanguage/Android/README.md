# Android Development

## Life Cycle
### Application
 - Foreground Process
 - Visible Process
 - Service Process
 - Cached Process

### Activity
![](https://developer.android.com/guide/components/images/activity_lifecycle.png)

## Class
### Context
#### 정의
 - Application 환경에 대한 전역 정보를 접근하기 위한 인터페이스.
 - 추상 클래스이며 실제 구현은 Android 시스템에 의해 제공된다.
 - Context를 통해 어플리케이션에 특화된 리소스나 클래스에 접근할 수 있다.
 - Activity 실행, Intent 브로드캐스팅 그리고 Intent 수신 등과 같은 응용 프로그램 수준의 작업을 수행하기 위한 API를 호출 할 수 있다.

#### 종류
 - Application(Application-life-cycle)
 - Activity(Activity-life-cycle)
 
Activity
 - Activity또는 Service가 실행 될때 기본Context에다 필요한 정보를 warp한다. 실행시 고유한 Context를 가지게 된다.
 
Service
 - Activity또는 Service가 실행 될때 기본Context에다 필요한 정보를 warp한다. 실행시 고유한 Context를 가지게 된다.

BroadcaseReceiver
 - onRecevie()시 Context를 가져올 수 있다. 이때의 Context는 ReveiverRestrictedContext이며 두가지 기능 registerReceiver()와 bindService()를 사용 할 수 없다. 리시버가 브로드캐스트를 처리 할때마다 새로운 Context가 생성 된다.


### 출처
[노블의 개발이야기](https://shnoble.tistory.com/57)