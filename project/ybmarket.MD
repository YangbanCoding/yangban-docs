# 미니 앱 - 양반마켓 : [중고거래]

## 요구사항
- 전화 번호 로그인
- 사진 업로드
- 실시간 채팅

## 페이지
1. 초기 화면
2. 전화 번호 인증 화면
3. 메인 탭1 : 상품 탭
4. 메인 탭2 : 채팅 탭
5. 메인 탭3 : 설정 탭
6. 상품 등록 화면
7. 상품 검색 화면
8. 상품 상세 화면
9. 채팅방 화면
10. 판매 내역 화면
11. 구매 내역 화면
12. 거래 완료 화면

## DB 테이블
- [user]\(id, phoneNumber, pushToken\)
- [product]\(id, isSold, name, price, text\)
- [chat]\(id, text\)
- [chatRoom]\(id\)

## 테이블 관계
- one to many
  - buyProduct [user] -> [product] 
  - sellProduct [user] -> [product]
  - chats [user] -> [chat]
  - chats [chatRoom] -> [chat]
  - productChatRooms [product] -> [chatRoom]
- many to many
  - userChatRooms [user] -> [chatRoom]

## 테스트
- 상품 등록
  - 상품 탭에서 + 버튼을 누르면 상품 등록 화면으로 이동한다
  - 상품 등록 화면에서 상품 사진과 제목, 내용, 가격을 작성하고 확인 버튼을 누르면 상품 탭에 상품이 추가된다
- 상품 검색
  - 상품 검색 화면에서 검색어를 입력하면 제목이나 내용에 검색어를 포함하는 모든 상품을 표시한다
- 상품 구매 연락
  - 상품 탭에서 원하는 상품을 누르면 상품 상세 화면으로 이동한다
  - 채팅으로 거래하기를 누르면 채팅창으로 이동한다
- 상품 판매 확정
  - 설정 화면에서 판매 내역을 누르면 판매 내역 화면으로 이동한다
  - 상품의 거래 완료 버튼을 누르면 거래 완료 화면으로 이동한다
  - 구매자를 선택하고 확인을 누르면 상품이 판매 완료로 변경된다
