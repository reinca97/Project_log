# uyoung-hompage

> - backend 없이 Cloud Firestore 사용하여 데이터 저장 (joomok2 계정 / 프로젝트명 동일 )
> - Admin 추가는 firestore 직접 접근하여 생성해야 함
>   * console > CloudFirestore> 'user' collection 선택
>   * 기존 문서 참고하여 신규 문서 추가 (반드시 auth: true 로 설정)


### public
- index.html :처음불러오는 html 파일, meta tag 수정은 여기서
- manifest.json : 프로젝트 정보
- robots.txt


### src > App.js
- 전체 state 관리 (redux 미사용)
- 컴포넌트 마운트 이후 firebase 시작/ 게시판 목록 가져오기/ 권한 체크
- getFilePathFromStorage : 게시판 조회해서 첨부파일 있을 경우 sorage > board 내의 그림파일 path 가져옴



### src > components
(다른 폴더는 특이점 없어서 생략)

<details>
    <summary>
        About
    </summary>

    최상단
    그림파일 원본 위에 가상선택자(&:before)로 어두운 레이어 만들어 덮음

</details>

<details>
    <summary>
        Admin
    </summary>

    최하단 우측 admin 버튼 눌렀을 때 뜨는 모달
    관리자로 등록된 email 주소 입력하면 로그인 링크를 보내도록 함
    (firebase email 인증 사용)
    관리자 등록방법은 문서 맨 첫 문단 참고

</details>

<details>
    <summary>
        Board
    </summary>

    * 주석처리부분은 초기 게시물 상세를 modal 띄워 보여주는 코드
      PostView 대신 AccordionList 사용함

    * Editor.js : 글쓰기 클릭시 보이는 모달창
      [주의] 파일 업로드는 CloudFirestore 가 아닌 Storage 의 board 폴더 내에 생성된 문서와 동일 id 로 저장됨

    

</details>

<details>
    <summary>
        Business
    </summary>
    단순 페이지/ 특이점 없음
</details>

<details>
    <summary>
        Contact
    </summary>

    send message 클릭시 Cloud Firestore > contact 에 내용 저장됨
    별도 실시간 알림이나 크론 없으므로 신규 메시지는 직접 로그인하여 확인해야함..

</details>

<details>
    <summary>
        Footer
    </summary>

    admin 모달 나오게 하는 버튼 있음

</details>

<details>
    <summary>
        Header
    </summary>
    
    - resizeWindow 에서 스크린 넓이별 섹션 높이 설정 

    - scrollToSection 은 resizeWindow 에서 설정된 높이에 따라 메뉴 버튼 눌렀을 때 세로 스크롤 이동시키는 함수
    
</details>

<details>
    <summary>
        Spinner
    </summary>

    로고와 깔맞춤한 스피너

</details>





