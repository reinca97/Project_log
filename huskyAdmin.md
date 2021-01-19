# Husky Admin

### Features
````````````````
huskyAdmin
 ├── README.md
 ├── node_modules
 ├── package.json
 ├── .gitignore
 ├── public
 │   ├── index.html
 │   └── manifest.json
 └── src
     ├── Actions
     ├── Constants
     ├── Images
     ├── lib
     ├── Reducers
     ├── App.scss
     ├── App.js
     ├── App.test.js
     ├── index.css
     ├── index.js
     ├── serviceWorker.js
     └── Components
          ├── Board
          ├── Category
          ├── CompanyCategory
          ├── Footer
          ├── Header
          ├── InnerComponents
          ├── JoinApproval       
          ├── Login      
          ├── Main     
          ├── Modals                                                             
          ├── Orders
          ├── Product
          ├── Retail                                                                                                                     
          └── RetailJoinApproval 
````````````````



<details>
    <summary>
        혹시 계실지 모를 , 이 코드를 상세히 보시고 수정하실 분을 위해..
    </summary> 

------------

 * 본 프로젝트와 uyoung-hompage 는 redux 및 react-redux 사용하지 않고 react 의 **createContext, useReducer** 를 사용하여 redux 와 유사하게 꾸몄습니다.

 >  - dispatch action --> change state(store).
 >  - 각 component 에서 Context 불러와서 store 값 접근

 *  root reducer 구현하기 위해 reduce-reducer(그냥 reducer 를 하나로 몰아주기만 함) 파일을 추가 하였습니다.


 * 왜 굳이 이렇게 했냐면.. 그때는 react-redux 에 Hooks (useDispatch/ useSelector) 가 없었어요 (7.2 에 등장). redux 설치 안하고 react 의 context 랑 useReducer 잘 쓰면 될 것 같아보여서 시도해본 것. 그냥 그땐 그러면 좋을 것 같아 보였음... 이후 프로젝트는 안티패턴일망정 정상적(?) 으로 redux,react-redux,thunk 사용하였습니다
--------------
- 혹시 npm start/yarn start 돌렸을때 node-sass 에러가 난다면 이는 필시
    1. node 버전 문제
    1. node-sass 버전 문제 (4.13.0)
    1. npm 버전 문제
    1. 운영체제 버전 문제 (일수도)
    
제 경우는 1,2,3 조치 후에도 고쳐지지 않아 (회사컴 작업 후 개인컴 - 카탈리나 10.15.6- 에서 발생) node-sass 삭제하고 scss 파일 수동 컴파일해서 css 파일로 만들어 붙였습니다.

-----------
끝
</details>




### src > lib 
 - "get-" 으로 시작하는 파일은 서버 요청용 (axios) 메소드 입니다.
    파일 이름은 get어쩌구 이지만 get/post/delete 다 있음.
   
- 주문 출력 테이블이나 엑셀 데이터 관리 원하는 경우 util.js 파일 수정.

