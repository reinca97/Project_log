#fishmarket-new
> tmi: 프로젝트명에 "new" 가 붙은 이유는 기존에 외부에서 django 로 제작된 페이지가 있었기 때문입니다...


### src > actions
    - reducers 폴더 내 파일명과 동일/ 해당 state 변경용 action creator

- data : 배송관련 데이터, 인보이스 데이터(배송사)
- deal : 거래 정보
- display
    * viewMode
    * toggleMenu : 메뉴 보이기/ 숨기기
    * displayModalName: 이름에 따라 해당 모달 보이기/ 빈 스트링이면 숨기기
    * currentMenu
    * asyncRequest: 비동기작업 상황(스피너 처리용)
- order : 주문 정보 
- saleRequest : 판매요청 리스트
- sales : 판매 정보 
- tempData : 주소 모달에서 사용하는 주소리스트, 사용자 인증 후 받아오는 정보 
- user : 유저 데이터/ 로그인 여부

### src > components
> ** 표시는 styled component (스타일 지정용)

<details>
    <summary>
        더보기
    </summary>

- Agreement : 회원가입시 약관 동의 화면
- Block ** 
- Button **
- CloseButton **
- DeliveryItemBlock : 상품별 출고증 발급 선택시 (건별 사용)
- DeliveryItemInputBlock : 출고증 발급 (전화번호 등 정보입력 화면)
- excelReader : 상품 일괄등록시 엑셀 업로드 부분. view(버튼)+기능
- Footer 
- GridBlock ** : GridTable 을 구성하는 작은 블록
- GridTable : 상세(주문) 현황 상단에 들어가는 테이블
- Hamburger ** : "냠냠"
- Header 
- index.js (컴포넌트 한번에 모듈화용 인덱스)
- Inline **
- Input **
- ItemInfoBlock : GridTable 구성요소
- Label **
- Modal ** (배경 가리고 모달 띄우는것만)
- Nav **
- RadioButtons **: 리스트 받아서 라디오 버튼 생성
- Select **
- SemiTitle **
- StatusBlock ** : 주문 상태별 색상 테마 지정
- Title **


</details>

### src > constants 

- terms : 이용약관 3종
- tableOption : 테이블 스타일 지정
- Theme
- index : redux 용 상수 및 firebase config


### src > pages 
> 별도 설명이 필요없는 항목은 파일명만 기재

<details>
    <summary>
        더보기
    </summary>

- AddressModal 
- CertifyModal : iframe event 사용해서 token 받아옴
- DealDetail : 상세 거래내역
- DealList
- DeliveryOrder : 출고증 인쇄 요청 화면 (주문 상품별로 출고증 인쇄 가능)
- DeliverOrderPDF : 출고증 모달 (canvas/팩스전송/출력버튼 포함)
- DeliveryOrderPDFPrint: 출고증 인쇄용 팝업
- DeliveryOrderPrint : 출고증 인쇄용(재발급시 상품별 리스트)
- FindPassword 
- Invoice : 운송장 인쇄화면
- InvoicePDF: 운송장 모달(canvas/팩스전송/인쇄 포함)
- Join 
- JoinComplete
- Loader : 스피너
- Login
- Main (삭제 가능)
- Menu : gnb
- Mypage
- OrderDetail
- OrderList
- RegisterItem : 신규 상품 등록
- Sales
- SalesDetail
- SOAPDF : 거래명세서 모달
- SOAPDF_APP: seayou app 용 거래명세서 (웹에서는 사용 X)
- Withdrawal : 탈퇴화면

</details>