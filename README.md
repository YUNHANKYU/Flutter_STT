# flutter_stt

Flutter STT(Speach to Text) Example 프로젝트입니다.
<p>
speach_to_text 플러그인을 사용한 예제입니다.

## Project init

- android

1. User Permission 세팅 <p>
안드로이드 세팅을 위해 프로젝트의 AndroidManifest.xml 파일에 user permission 을 추가해준다.<p>
경로: <project root>/android/app/src/main/AndroidManifest.xml<p>
    ```
    <uses-permission android:name="android.permission.RECORD_AUDIO"/>
    <uses-permission android:name="android.permission.INTERNET"/>
    <uses-permission android:name="android.permission.BLUETOOTH"/>
    <uses-permission android:name="android.permission.BLUETOOTH_ADMIN"/>
    <uses-permission android:name="android.permission.BLUETOOTH_CONNECT"/>
    ```

2. Anroid SDK 30 or later<p>
안드로이드 targetSDKVersion 을 30 or later 로 맞춰준다. 그리고 프로젝트의 AndroidManifest.xml 파일에서 위 1번에서 추가한 permissions 다음으로 아래 코드를 추가해준다.

    ```
    <queries>
        <intent>
            <action android:name="android.speech.RecognitionService" />
        </intent>
    </queries>
    ```


- ios

1. info.plist 파일에 아래 key 쌍을 추가한다.<p>
    ```
    <key>NSSpeechRecognitionUsageDescription</key>
    <string>음성인식을 위해 필요합니다.</string>
    <key>NSMicrophoneUsageDescription</key>
    <string>음성인식을 위해 마이크 권한이 필요합니다.</string>
    ```