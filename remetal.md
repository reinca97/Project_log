#Re-metal

> Remetal 은 테이블(표) 및 페이지네이션 자체 컴포넌트 사용,
> (Components > InnerComponents > Table / TableWithPagination)
>
> Remetal admin 은 [material table](https://material-table.com)을 사용하였습니다.


### public
- index.html : 가장 상위 레벨 html 파일 / 로고, 아이콘, 메타테그는 여기서 수정
- firebase-messaging-sw.js : cloud message 추가용 파일
- logo.ico
- manifest.json
- robots.txt



### src
<details>
    <summary>
        Action
    </summary>

- index
- contract (계약 관련)
- data
- display
- help-center
- tempData
- user
- utils

</details>

<details>
    <summary>
        Components
    </summary>

- Alarm 
- FindId
- FindPassword
- FloatTable : 메인페이지 우측 거래내역 표시 테이블
- Footer
- Guide : 서비스 가이드, 가격가이드 페이지
- Header
- HelpCenter : 고객센터 3종
- InnerComponents : 버튼, 페이지 파이틀 등 반복 사용하는 작은 컴포넌트 모음
    > - TableWithPagination 
    >   * index : 기본 테이블+하단 페이지네이션 (리스트 10개씩 표시)
    >   * DealerListTableWithPagination : 회원정보 > 거래정회원 정보조회/변경 테이블 + 페이지네이션
    >   * PaymentPendingListTable : 결제대기리스트 테이블 + 페이지네이션

    > - Table : 서버에서 받은 데이터를 array 로 변경하여 head 제외 table body    에 뿌림. (순서 중요)
    >   * DealerListTable : 회원정보> 거래정회우너 정보 조회/변경 테이블 (결제요청 가능여부 select 란 있음)
    >   * Table : 기본형 테이블  
    >   * TableWithCheckbox : 체크박스(다중선택) 있는 테이블
  

- Join
- Main
- Marker : 메인페이지 지도위에 표시되는 마커
- Modals : 각종 모달 모음 (store.display.displayModalName 에서 지정된 모달 표시. 빈 스트링이면 모달 감춤)
  
> - Certify : 실명인증부분. 외부 iframe 에서 message event 로 key 받아서 유저 정보 GET 요청함.
> 
> - PaymentAlarm : 화면설계서 및 디자인에 있어 구성했으나 실제 페이지상 구현 X (displayModalName 을 payment 로 바꾸면 디스플레이는 가능)
> 
- MyPage
- Nav
- Payment : 결제 페이지 관련
- Sidebar

</details>

<details>
    <summary>
        Constants
    </summary>

- fcm.js : firebase config 
- index.js : Redux 및 api 요청용 상수 모음
</details>

<details>
    <summary>
        Fonts
    </summary>
</details>

<details>
    <summary>
        lib
    </summary>

- localStorage.js/ SessionStorage.js : 브라우저 로컬/세션 스토리지용 method
- MakeContractPdf.js : 물품공급계약서 생성용 파일. original/copy 2본 생성하고 original 만 디피함
- utils.js :  (파일 내 주석 참고)
</details>

<details>
    <summary>
        Reducers
    </summary>

Action 과 파일 이름 일치하는 각각의 reducer 파일
</details>

<details>
    <summary>
        Requests
    </summary>
 각 페이지 or 기능별 Api 요청 파일들

- alarm
- contract
- data
- deal
- help-center
- payment
- user
- user-join
- utils




</details>
