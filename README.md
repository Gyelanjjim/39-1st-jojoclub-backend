# WEMALONE

<img src="https://i.ibb.co/725kkWj/2022-11-28-1-23-00.png"
/>


## 📈 프로젝트 소개
[데모 영상 링크](https://youtu.be/cUgrQdEAlaM)
<p>
향수 판매 웹사이트(Jomalone)을 모델링 한 프로젝트. <br />
Smell is a word, perfume is literature. <br />
다양한 향의 향수를 소개합니다. 소중한 사람들에게 선물하세요. <br /> 
필터링을 통해 원하는 향을 찾아보세요. <br />
내가 고른 향에 scent fairing을 추천받아보세요.<p>


## 👥 개발인원
- Front-end 강지민, 남연우, 송아영, 이유주(4명), Back-end 송철진, 임창현(2명)

## 📆 기간
- 2022/11/14 ~ 2022/11/25
  
## 🛠️ 기술 Stack

### Front-End
<div>
  <img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=white">
  <img src="https://img.shields.io/badge/react-61DAFB?style=for-the-badge&logo=react&logoColor=white">
  <img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white">
  <img src="https://img.shields.io/badge/sass-CC6699?style=for-the-badge&logo=sass&logoColor=white">
  <img src="https://img.shields.io/badge/css3-1572B6?style=for-the-badge&logo=css3&logoColor=white">
  <img src="https://img.shields.io/badge/git-F05032?style=for-the-badge&logo=git&logoColor=white">
</div>

### Back-End
<div>
  <img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=white">
  <img src="https://img.shields.io/badge/nodejs-339933?style=for-the-badge&logo=git&logoColor=white">
  <img src="https://img.shields.io/badge/express-000000?style=for-the-badge&logo=express&logoColor=white">
  <img src="https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=white">
  <img src="https://img.shields.io/badge/git-F05032?style=for-the-badge&logo=git&logoColor=white">
</div>

### Common
- common : Git, GitHub, AWS, Prettier, TablePlus
- 협업툴 : Notion, Slack, Trello, PostMan, DBdiagram

## ✅ 구현  
<table>
  <th>기능</th>
  <th>설명</th>
  <th>담당 개발자</th>
  <tr>
    <td>Sign up</td>
    <td>정규 표현식, Bcrypt을 사용한 회원가입 구현</td>
    <td>임창현, 송철진</td>    
  </tr>
    <tr>
    <td>Sign in</td>
    <td>정규 표현식, Bcrypt, JWT를 활용한 로그인 구현</td>
    <td>임창현, 송철진</td>    
  </tr>
  </tr>
    <tr>
    <td>Filter</td>
    <td>SQL IN, queryString을 활용한 필터링 기능 구현</td>
    <td>main : 송철진 sub : 임창현</td>    
  </tr>
  </tr>
    <tr>
    <td>Product Detail</td>
    <td>제품별 사이즈 조회 및 가격 조회 기능 구현</td>
    <td>임창현, 송철진</td>    
  </tr>
  </tr>
    <tr>
    <td>Cart</td>
    <td>장바구니 기능 구현</td>
    <td>임창현</td>    
  </tr>
  </tr>
    <tr>
    <td>Order</td>
    <td>주문내역 조회기능 구현</td>
    <td>임창현</td>    
  </tr>
</table>

## ⭐️ 담당 업무
1. **이메일, 비밀번호 유효성 검증 기능**
  - 유효하지 않은 이메일 또는 비밀번호를 클라이언트로부터 입력받았을 때 상태코드(400)와 에러 메시지를 반환시키기 위해 정규표현식을 사용하여 유효성 검증 기능을 구현했습니다. 
  - 해당 기능은 회원가입과 로그인 API에서 모두 사용될 수 있으므로 재사용성을 고려하여 utils폴더에 별도 구현했습니다.
2. **회원가입 API** 
  - 중복된 이메일로 가입할 수 없도록 클라이언트로부터 입력받은 이메일 값으로 DB를 조회하여 해당 값이 존재하면 상태코드(400)와 에러 메시지를 반환하도록 구현했습니다.
  - 악의적 내부 DB관리자에 의한 개인정보 유출과 레인보우 테이블 공격을 방지하기 위해 클라이언트로부터 입력받은 비밀번호를 bcrypt 해시 처리된 값을 DB에 저장하도록 구현했습니다.
3. **로그인 API**
  - 서버 상태를 stateless하게 유지하여 서버확장에 유리하고, 클라이언트가 서버에 요청 시 Cookie를 전달하지 않아 CSRF 등의 악성공격에 유리하기 때문에 토큰 기반 인증 방식(JWT)을 사용해 구현했습니다. 
  - 인증된 ID를 여러 API에서 활용하기 위해 Payload에 userId를 담아 응답하도록 구현했습니다
  - 클라이언트로부터 입력받은 이메일이 DB에 존재하지 않을 때 적절한 상태코드(404)와 에러메시지를 반환하도록 구현했습니다
  - 로그인 시 클라이언트로부터 입력받은 비밀번호와 회원가입 시 암호화되어 DB에 저장된 비밀번호의 일치 여부를 확인하고 불일치할 경우 적절한 상태코드(401)와 에러메시지를 반환하도록 구현했습니다.
  
4. **필터링된 상품 목록 조회 API**
- 여러 조건에 따라 상품을 조회하려면 클릭 수가 많은 기존 사이트를 보완하는데 초점을 두었습니다. 
- 필터링 조건에 따라 한 페이지 내에서 한 눈에 보여줄 수 있도록 클라이언트가 향기(scent)와 성별(gender)이라는 각 필터링 조건을 단일 또는 다중 선택하여 요청하면 `SQL IN` 연산자와 쿼리 스트링을 사용해 DB에서 조회한 결과와 상태코드를 응답하도록 구현했습니다.
- 클라이언트가 자유롭게 선택하여 특정 Column을 기준으로 정렬된 값 요청 시 응답할 수 있도록 `SQL ORDER BY` 쿼리를 사용해 기능을 구현했습니다
- 클라이언트가 자유롭게 선택하여 특정 제품 범위를 요청 시 `SQL LIMIT, OFFSET` 쿼리를 사용해 적절한 상태코드와 값을 응답하는 기능을 구현했습니다

5. **상품 상세 조회 API**
- 클라이언트가 상품 옵션 ID를 담아 요청 시, 해당된 하나의 상품 상세 내용과 각 용량 및 이미지를 JSON 객체로 묶어 적절한 상태코드와 값을 응답하도록 기능을 구현했습니다. 


## ERD

<img src="https://i.ibb.co/dMS17x2/2022-11-28-1-44-17.png" >

<h2>
일정관리(Trello, Notion)</h2>
<hr>
<img src="https://i.ibb.co/92FWD0C/2022-11-28-1-28-42.png">
<img src="https://i.ibb.co/HxX3bnj/2022-11-28-1-31-24.png">

## Reference

- 이 프로젝트는 [Jomalone](https://www.jomalone.com) 사이트를 참조하여 학습목적으로 만들었습니다.
- 실무수준의 프로젝트이지만 학습용으로 만들었기 때문에 이 코드를 활용하여 이득을 취하거나 무단 배포할 경우 법적으로 문제될 수 있습니다.
- 이 프로젝트에서 사용하고 있는 사진 대부분은 위코드에서 구매한 것이므로 해당 프로젝트 외부인이 사용할 수 없습니다.
