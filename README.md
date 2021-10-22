# 김정진(Jeongjin Kim)

> ### 문제해결에 집착하는 개발자, 김정진입니다!
>
> <br />
> <img src='https://user-images.githubusercontent.com/79352105/136808119-e5843d4a-e238-4207-8056-dc1163690dff.jpg' alt='증명사진' width=200, height=260>

- 이메일 : jeongjin.jj.kim@gmail.com
  <br />
  <br />

## Projects

- <a href="#tennis365">쇼핑몰 사이트</span>
- <a href="#portfolio">치과위생사 포트폴리오 사이트 의뢰</span>

<br />

## <span id="tennis365">쇼핑몰 사이트(Tennis 365)</span>

### <a href="https://sleepy-austin-0254fa.netlify.app/">사이트 바로가기</a>

### <a href="https://github.com/flexing1010/Tennis365/blob/main/README.md">깃허브 페이지</a>

![365-main1](https://user-images.githubusercontent.com/79352105/137228810-62e88c17-1c7a-499e-b6e9-b10d8a6de1e6.gif)

### 개발 주요 사항

> - 프로젝트의 기획, 프론트엔드/백엔드/DB 설계와 개발, 배포까지 풀 사이클로 개발
> - JWT를 사용하여 토큰 기반 사용자 인증
> - 프론트엔드에서 관리자가 상품이미지를 등록하면 백엔드에서 Multer를 통해 해당 파일을 Amazon s3에 저장
> - 아임포트를 사용하여 결제기능 구현(테스트 계정)
> - PC, 노트북, 모바일 환경을 고려한 반응형 사이트
> - Netlify(프론트엔드), Heroku(백엔드)를 통한 서비스배포

### 기술 스택

> Frontend: JavaScript / React / SASS(SCSS)  
> Backend: Node.js / Express / MySQL \
> Deployment: Netlify / Heroku

### 문제해결 사례

1. 허가받지 않은 사용자가 특정 URL에 접근하는 것을 방지하는 URL 보호 기능
   - 문제: 마이페이지, 주문/결제 같이 특정 사용자만을 위한 페이지를 URL을 직접 입력하면 누구든지 접근할 수 있는 문제
   - 원인: URL에 현재 사용자의 권한을 확인하는 장치가 없음
   - 해결 과정: 관련 내용을 검색한 끝에 React에서는 react-router를 사용해야 한다는 걸 발견한 후, 찾은 내용들과 공식 문서를 학습
   - 해결:
     - react-router의 Route, Redirect를 포함한 PrivateRoute 컴포넌트를 만들고 그 안에서 토큰의 유무로 사용자를 인증한다
     - 인증이 성공하면 해당 페이지를 렌더링하고 실패한다면 로그인 페이지로 Redirect 한다.
     - 이 방법만으로는 사용자 인증(Authentication)만 하고 인가(Authorization)는 할 수 없다(로그인한 다른 사용자의 접근을 막지 못함)
     - PrivateRoute에서 인증과 인가를 동시에 하게 하려 했으나 실패
     - 결국 인가는 이동하려는 url의 param에 있는 사용자 id와 서버로부터 받은 사용자 id 정보를 비교하는 방법으로 페이지 내에서 해결
   - 비고: 이 문제를 해결하는 동안 가장 고민한 부분은 PrivateRoute에서 인증/인가를 동시에 하게 하는 부분이었습니다. 생각지 못했던 부분에 막혀서 꿈에 나올 정도로 계속 고민한 끝에 인가 기능을 이동하려는 페이지에서 처리하는 방법을 생각했습니다. 문제 해결에는 어떻게든 해결하겠다는 집착과 다양한 답을 생각할 수 있는 넓은 시야의 중요성을 느낄 수 있었던 경험이었습니다.

<br />
<br />

## <span id="portfolio">치과위생사 포트폴리오 사이트 의뢰</span>

### <a href="https://flexing1010.github.io/Jinah-s-Portfolio-Website/">사이트 바로가기</a>

### <a href="https://github.com/flexing1010/Jinah-s-Portfolio-Website">깃허브 페이지</a>

<br />

### 개발 주요 사항

> - 프리랜서 활동 중인 치과위생사의 의뢰로 만든 포트폴리오 사이트
> - 모바일 환경을 우선시한 반응형 웹 사이트
> - 재사용성을 고려하여 캐러셀 슬라이드를 함수화하여 사용

### 기술 스택

> Frontend: JavaScript / HTML / CSS  
> Deployment: GitHub Pages

### 문제해결 사례

1. 의뢰인과의 커뮤니케이션 문제 개선 사례
   - 문제: 개발 초반부에 의뢰인과의 커뮤니케이션이 원활하지 않아 개발이 더디어짐
   - 원인: 의뢰인의 의견이 필요하면 그때그때 피드백을 요청하는 방식이어서 기다려야 하는 일이 많아짐(일주일 최대 4번까지)
   - 해결:
     - 의뢰인과의 회의를 통해 최대한 디테일하게 아웃라인을 만듦
     - 합의된 아웃라인이 있기 때문에 피드백을 기다리는 동안 개발이 멈추는 일이 없어짐
     - 회의 이후 피드백 요청이 일주일 최대 1번 정도로 줄어듦
   - 비고: 개별 개발 의뢰를 받아 위에 언급한 문제뿐만 아니라 비개발자인 의뢰인과의 커뮤니케이션 문제 등 신입 개발자 신분에서 쉽게 느낄 수 없는 문제를 해결하는 과정에서 많은 것을 배울 수 있었던 경험이었습니다.
