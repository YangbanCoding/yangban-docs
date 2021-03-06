# 미니 앱 - 양반톡v0.1 : 메신저

## 앱 다운로드
- [구글 플레이](https://play.google.com/store/apps/details?id=com.yangbancoding.ybtalk)
- [앱 스토어](https://testflight.apple.com/join/Zlc4Yfd3)

## 개발 순서
1. 요구 사항 파악
2. 핵심 기능 선정
3. 데이터 베이스 설계
4. 화면 정의
5. 요소 선언 (HTML)
6. 디자인 (CSS)
7. 기능 구현 (Javscript)
8. 테스트

## 요구사항
- 실시간으로 채팅이 가능한 앱을 만들고 싶다!

## 주요 기능
- 소셜 로그인
- 친구 추가
- 실시간 채팅
- 푸시 알림

## 미구현 기능
- 친구 삭제
- 메시지 차단
- 채팅방 나가기
- 이름, 프로필 사진 변경
- 수신 확인
- 딥 링킹(푸시 알림 누르면 바로 채팅방으로 이동)
- 인앱 푸시 알림

## 데이터
- 유저 (로그인 정보)
- 채팅 (채팅 메세지)
- 채팅방

## 데이터 관계
- 일 대 다
  - 유저 -> 채팅 (유저는 채팅을 여러 개 할 수 있다)
  - 채팅방 -> 채팅 (채팅방은 채팅이 여러 개 있다)
- 다 대 다
  - 유저 <-> 유저 (친구 추가하기)
  - 유저 <-> 채팅방 (여러 명의 유저가 여러 개의 채팅방에 들어간다)

## 페이지
1. 로그인 페이지
2. 메인 탭1 : 친구 목록 탭
3. 메인 탭2 : 채팅방 목록 탭
4. 메인 탭3 : 설정 탭 
5. 친구 추가 페이지
6. 친구 상세 페이지
7. 채팅방 페이지

## 테스트
- 로그인 테스트
  - 구글 아이디로 로그인에 성공한다
- 친구 추가 테스트
  - 구글 이메일로 친구를 추가한다
- 채팅 테스트
  - 다른 유저가 채팅방에 쓴 메세지를 실시간으로 확인 가능하다
- 푸시 알림 테스트
  - 앱을 껐을 때 다른 유저가 메세지를 쓸 경우 푸시 알림이 온다
