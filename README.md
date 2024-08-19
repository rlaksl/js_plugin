# Javascript Plugin
## 공통 주의사항
* 각 플러그인 사용 시 해당 플러그인의 필수 연결파일 먼저 확인하기!
* css, js 파일 확장자가 서로 다른 경우가 있으니 이름과 함께 확장자 반드시 확인
## Swiper
* swiper, swiper-wrapper, swiper-slide
* 위 3개의 클래스명은 swiper 적용 기본 명칭이므로 받느시 수정없이 그대로 작성하기
* 위 공통 명칭 외에 각 swiper 구분용으로 `div class="swiper"` 시작태그에 한 칸 띄우고
별도의 구분용 클래스 적용하기 ex) `div class="swiper mainSlide"`
* swiper 플러그인 적용 대상에 nth 관련 수열선택자 사용하지 않기
* ` swiper-slide`를 개별로 구분하고 싶다면? nth 수열선택자 사용하지 않고 개별 클래서 적용해서
디자인 또는 동적 결과 사용하기 예) `div class="swiper-slide slide1"`
* swiper 적용 대상에 원하는 태그 추가는 swiper-slide 안에서만 사용하기(태그 제한 없음)
### Swiper css 주의사항
* swiper, swiper-wrapper, swiper-slide
* 위 기본 클래스명 기준 swiper, swiper-wrapper 기본 css가 내장되어있기 때문에
반드시 그 점을 체크하고 원하는 css를 설정해야 한다.
* 공통 swiper 클래스 대상 기준 사용 가능한 css list
: `width, margin, padding, position, transform, 꾸미는 속성(background, color, font,...)`
* 공통 swiper,swiper-wrapper 클래스에 flex 설정 금지
* 공통 swiper-wrapper 금지 속성
: 관련한 속성들(position, flex, float, width, height, margin(padding은 가능))
### Swiper option css 주의사항
* prev, next, pagination, scroll-bar
* 위 옵션들은 필요한 경우에만 선택적으로 작성한다.
* 기본적으로 swiper 시작태그의 자식 요소로 작성한다.
* swiper 시작 태그의 바깥쪽 위치로 디자인하고 싶은 경우에만 swiper 바깥쪽 위치에
태그를 구성하고, 해닥 위치의 새로운 부모 대상에 position:relative를 설정한다.
(swiper 옵션들에 absolute가 내장되어 있기 때문)


*  **`swiper-wrapper` 안에는 `swiper-slide`만 들어갈 수 있음.**
추가 옵션 태그는 반드시 swiper-wrapper 밖에 생성
* `.swiper-pagination-bullet`: **css 수정**할 때 클래스명 뒤에 **-bullet** 붙이기. 그리고 면으로 인식하기 때문에 색 바꾸려면 color말고 background로 줘야 함. 기본적으로 opacity가 내장되어 있음
* `.swiper-pagination-bullet-active`: **활성화** 되어 있는 **페이저만 색** 바꾸고 싶으면 **-bullet-active**
* `.swiper-scrollbar`: scrollbar도 마찬가지로 색 바꾸려면 background
* `.swiper-scrollbar-drag`: **-drag** 붙여주면 **활성화되는 bar**에 색 다르게 넣을 수 있음