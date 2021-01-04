#Re-metal Admin

> Remetal 은 테이블(표) 및 페이지네이션 자체 컴포넌트 사용,
> 
> Remetal admin 은 [material table](https://material-table.com)을 사용하였습니다.



### public
- (remetal 과 동일)


### src
<details>
    <summary>
        Action
    </summary>

- account
- contract
- customer
- deals
- display
- helpCenter
- payment
- trade
- user
- utils
</details>

<details>
    <summary>
        Components
    </summary>

- Account
    - DepositCheck
    - DepositList
- Contract
- DashBoard
- Header
- HelpCenter
- JoinApproval
- Miscellaneous
- Modals
- Nav
- Payment
- Trade
- UserList
</details>

<details>
    <summary>
        Constants
    </summary>

- columns : 회원등급별 material table column
- fcm : firebase config 
- menuList : 유저(admin)에 따른 메뉴 리스트 (은행 사용자는 계약정보 및 결제 메뉴만 보여줌)
- theme : table styles
- url
</details>

<details>
    <summary>
        Fonts
    </summary>
</details>

<details>
    <summary>
        Images
    </summary>
</details>

<details>
    <summary>
        lib
    </summary>

  local/session storage 의 편한 사용을 위한 method 정의

</details>

<details>
    <summary>
        Reducers
    </summary>

Action 과 파일 이름 일치하는 각각의 reducer 파일

</details>

<details>
    <summary>
        Request
    </summary>

 각 페이지 or 기능별 Api 요청 파일들

</details>

