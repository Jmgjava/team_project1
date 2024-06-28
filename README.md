![transparent](https://capsule-render.vercel.app/api?type=waving&color=B4E1F8&fontColor=fff&text=🛒이팀저팀&height=250&fontSize=70&descAlignY=80&descAlign=70)


<br>

<h2 align="center" style="color:#96b3d9"> 쇼핑몰& 관리자 모드 기반 챗봇 구현 </h2>

<br>


## 📕프로젝트 소개

- 관광상품을 판매하는 사이트
- 판매자와 구매자를 나누어서 판매자는 판매가 가능하고 구매자는 구경 및 장바구니 담기가 가능

| 작업파일                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|
| [쇼핑몰& 관리자 모드 기반 챗봇 구현](https://github.com/Jmgjava/team_project1/tree/master/shoppingMall_project) |

<br>

## 💻사용프로그램

<span>
<img src="https://img.shields.io/badge/intellij IDEA-000000?style=flat&logo=intellij IDEA&logoColor=white"/> 
<img src="https://img.shields.io/badge/visualstudio-0075c6?style=flat&logo=visualstudio&logoColor=white"/> 
</span>
<br>
<span>
<img src="https://img.shields.io/badge/java-007396?style=flat&logo=java&logoColor=white"/> 
<img src="https://img.shields.io/badge/gradle-02303A?style=flat&logo=gradle&logoColor=white"/>
<img src="https://img.shields.io/badge/mysql-4479A1?style=flat&logo=mysql&logoColor=white"/> 
</span>
<br>
<span>
<img src="https://img.shields.io/badge/springboot-6DB33F?style=flat&logo=springboot&logoColor=white"/>
<img src="https://img.shields.io/badge/springsecurity-6DB33F?style=flat&logo=springsecurity&logoColor=white"/>
<img src="https://img.shields.io/badge/spring data JPA-6DB33F?style=flat&logo=spring data JPA&logoColor=white"/> 
</span>
<br>
<span>
<img src="https://img.shields.io/badge/html5-E34F26?style=flat&logo=html5&logoColor=white"/>
<img src="https://img.shields.io/badge/css3-1572B6?style=flat&logo=css3&logoColor=white"/>
<img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=JavaScript&logoColor=white"/> 
</span>
<br>
<span>
<img src="https://img.shields.io/badge/kakaoMap-FFCD00?style=flat&logo=kakao&logoColor=white"/>
<img src="https://img.shields.io/badge/thymeleaf-005F0F?style=flat&logo=thymeleaf&logoColor=white"/>
<img src="https://img.shields.io/badge/jquery-0769AD?style=flat&logo=jquery&logoColor=white"/> <br>
<img src="https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazonwebservices&logoColor=white"/>
</span>
<br>

## 📁ERD
![img_3.png](img/img_3.png)

<br>

## 🙍‍♂️팀원
|이름| 작업 |
|--|----|
|조민근| OAuth2, DB설계, kakaoMap api, CICD, 인기순위|
|정**|reply, 프론트, Q&A 프론트|
|왕**|Member(회원) CRUD|
|박**|Board(상품)  CRUD, ( 장바구니 ) CRUD|
|서**|shopList, ADMIN 창( Member, Board 창 삭제,수정)|

<br>

## ✍작업내용

- [**DB설계**](#DB-설계)
    - 데이터베이스설계
- [**Oauth2, 로그인**](#Oauth2-로그인)
    - 아이디 비번 및 kakao, google, naver 로그인
    - 로그인 성공 및 실패시 event
- [**kakaoMap API**](#kakaoMap-API)
    - Daum 주소 API 활용
    - 카카오 지도 및 marker 구현
- [**인기순위**](#인기순위)
    - 관광상품 조회수를 기준으로 순위구현

<br>

### DB 설계

- **회원(구매자, 판매자)** 은 **여러개의 상품** 을 **장바구니**에 담음
- **회원(구매자, 판매자)** 은 **여러개의 댓글**을 작성할 수 있음
- **회원(판매자)** 은 **여러 개의 상품** 을 올릴 수 있음

![img_3.png](/img/img_3.png)

### Oauth2, 로그인

- 로그인 성공 시 성공메세지 화면에 표시
- 로그인 실패 시 예외처리 후 html 로 표현
- oauth2 로 소셜 로그인 구현

| 로그인 실패 시                                                                                               |
|--------------------------------------------------------------------------------------------------------|
| ![fail](https://github.com/Jmgjava/team_project1/assets/154856565/b1c891a0-fcaa-4371-9c52-eab275b34f23) |

| 로그인 성공 시                                                                                                  |
|-----------------------------------------------------------------------------------------------------------|
| ![success](https://github.com/Jmgjava/team_project1/assets/154856565/bd1e4564-3143-4b6f-9d04-f2041fe9b4cf) |

| google, naver, kakao 로그인                                                                                 |
|----------------------------------------------------------------------------------------------------------|
| ![oauth2](https://github.com/Jmgjava/team_project1/assets/154856565/dd58715b-2bd9-4190-9edc-0a7307d1bde5) |

### kakaoMap API

- Daum 주소 API 사용해 주소창 입력
- 입력한 주소 kakaoMap 으로 위도, 경도 찾아 마커 구현

| **Daum 주소 API** 활용해 주소창을 입력  |
|------------------------------|
| ![img_5.png](/img/img_5.png) |

| kakaoMap API 사용                                                                                            |
|------------------------------------------------------------------------------------------------------------|
| ![kakaoMap](https://github.com/Jmgjava/team_project1/assets/154856565/dae97fac-96d1-469b-bbac-ae565e18b0c1) |

### 인기순위

- 상품의 조회수순으로 순위를 만들어 등수를 매김

| top3 인기순위                                                                                            |
|------------------------------------------------------------------------------------------------------|
| ![hot](https://github.com/Jmgjava/team_project1/assets/154856565/f25420a6-eda8-4e19-aa06-dcc3b7427ec0) |

| 클릭시 선택한 등수 페이지로 이동                                                                                       |
  |---------------------------------------------------------------------------------------------------------------|
| ![hot_details](https://github.com/Jmgjava/team_project1/assets/154856565/cb3a15a9-8860-4c39-bda9-cda2fd629696) |

<br>

![transparent](https://capsule-render.vercel.app/api?type=soft&color=6B4D9F&fontColor=fff&text=감사합니다.&animation=fadeIn&height=100&fontSize=40&descAlignY=80&descAlign=70)
