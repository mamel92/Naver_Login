# HTML/CSS 코딩 테스트

## HTML 작성 시 요구 사항
- 기본 언어 명시
- 적절한 타이틀(&lt;title&gt;) 작성
- 논리적인 순서를 고려하여 마크업
- 시맨틱 마크업   
(클래스 네이밍은 자유, 단 <span style="color: #f00">.is--invalid</span> 예외)  

- 문법 오류가 발생하지 않도록 작성
- 1개 이상의 제목(heading) 요소 사용
- 로고는 &lt;img&gt; 요소로 마크업하고 해당 로고 클릭 시 네이버 홈페이지로 이동하도록 구현  
(네이버 홈 : https://www.naver.com/)  

- 로고 이미지는 배경이 아닌 &lt;img&gt; 요소로 마크업  
(svg를 지원하는 웹브라우저는 svg 형식으로 그렇지 않은 웹브라우저는 png 형식으로 보여지도록 구현)  

- 웹접근성을 고려한 로그인 폼 서식 마크업  
(레이블 제공의 경우 WAI-ARIA가 아닌 HTML 네이티브 방식으로 구현)  

- 아이디와 비밀번호는 필수 입력 서식임을 알 수 있도록 구현  
- 아이디와 비밀번호 입력 값이 오류일 때(.is--invalid) 에러 메시지가 보이도록 구현   
(CSS에서 display: none과 block으로 처리할 것)  

- IP 보안 텍스트 클릭 시 미리 제공 된 ip_secruity.html 파일이 새창에 보이도록 구현  
(새창 링크 시 보안 이슈를 해결하기 위한 값도 설정해야 함)  

- IP 보안 체크박스의 ON/OFF 텍스트는 CSS의 ::before 또는 ::after 등의 가상 요소를 사용하여 구현  

<div style="padding: 1em; background: #e9f0fd; border-left: 10px solid #42b983">
&#8251; 아이디와 비밀번호 입력 값이 오류일 때 해당 <span style="color:#f00;font-weight: bold">&lt;input&gt; 요소에 .is--invalid가 추가되도록 하는 기능</span>은 미리 자바스크립트 파일에 구현되어 있음.  

&#8251; 제공 된 <span style="color: #00f; font-weight: bold">form_validation.js</span> 파일을 HTML에 적용 후 <span style="color: #00f; font-weight: bold">로그인 버튼을 클릭</span>하면 해당 클래스가 추가된 상황을 확인할 수 있음.
</div>


## CSS 작성 시 요구 사항
- 반응형으로 구현 (768px 미만 모바일 / 768px 이상 데스크탑)
- 모바일 퍼스트 (공통 스타일과 모바일 스타일을 먼저 구현한 후 데스크탑 스타일을 재정의 할 것)  
- 스타일 구현 시 height 속성을 이용하여 높이를 고정하지 말 것  
- 글자 크기 및 여백(margin 및 padding)은 모두 rem 단위로 설정할 것  
html 요소의 font-size는 10px로 설정되어 있음.  

- 기본 글자 크기 및 색상  
16px, #181818  

- 로고  
가로 230px, 가운데 배치  
로고 이미지는 반응형으로 처리하여 가로 크기에 맞게 높이는 자동 조절되도록 설정  

- 포커스 스타일 커스텀  
아웃라인 제거 후 그림자 스타일로 아웃라인 효과 구현(그림자 색상 #24388d)  

- 포커스 상태이지만 포커스 비저블이 아닐 때  
아웃라인 효과 대신 적용한 그림자 스타일 제거  

- 모바일 로그인 폼
로그인 폼의 가로 크기는 100%(좌/우 여백 각 20px 포함)  
IP 보안 ON/OFF 영역은 보이지 않도록 구현  
로그인 상태유지는 오른쪽 정렬  

- 데스크탑 로그인 폼  
로그인 폼의 가로 크기는 500px(좌/우 여백 각 20px 포함)  
로그인 상태유지는 왼쪽 정렬, IP 보안 ON/OFF 영역은 오른쪽 정렬  

- 입력 서식 글자크기 및 세로 크기, 테두리 선 색상, 배경 색상  
기본 상태 : 14px, 45px, #dadada, #fff  
포커스 상태 : #03cf5d, #e9f0fd  
**(입력 서식에 포커스 시 커스텀 포커스 아웃라인 스타일인 그림자 효과 대신 테두리 선 색상과 배경 색상만 변경되도록 구현)**  

 - 오류 메시지 글자 크기, 글자 색상, 위쪽 여백  
12px, #ff1414, 5px  
아이디 및 입력 서식에 .is--invalid가 있을 경우 오류 메시지가 보이도록 구현  

- 로그인 버튼 글자 크기, 세로 크기, 글자 색상, 배경색상, 위쪽 여백  
16px, 45px, #fff, #03cf5d, 20px 

- 로그인 상태유지 및 IP 보안 ON/OFF 영역 위쪽 여백  
10px  

- 로그인 상태유지 체크박스 배경 이미지 및 크기와 여백  
선택안함 : icon-unchecked.svg   
선택함 : icon-checked.svg  
가로 * 세로 : 24px * 24px  
배경 이미지 오른쪽 여백 : 5px  
(키보드 포커스 시 포커스 커스텀 스타일이 적용되어야 하지만 포커스 비저블 시 아웃라인 스타일이 적용되지 않도록 구현)

- IP 보안 글자 크기, 글자 색상
16px, #181818 

- IP 보안 체크박스 가상 요소 콘텐츠
선택안함: OFF  
선택함: ON  
(키보드 포커스 시 포커스 커스텀 스타일이 적용되어야 하지만 포커스 비저블 시 아웃라인 스타일이 적용되지 않도록 구현)