# Ajou-Univ-coronic-travel-path-

<h3>아주대학교 교내 확진자 발생 현황 및 교내 이동 경로를 쉽고 직관적으로 볼 수 있도록 하는 웹사이트 개발 프로젝트입니다.</h3>

https://wkazxf.github.io/Ajou-Univ-coronic-travel-path-/
<br><br>
<h3>Description></h3>


![image](https://user-images.githubusercontent.com/84431962/130308606-73989357-80bb-44b8-9867-bc9cd5ace276.png)

-코로나 학교 대응 안내, 아주대학교 로고, COVID19(질병관리청) 클릭 시 배너처럼 각 링크로 이동할 수 있게끔 a태그를 활용.

-아주대학교 로고는 마땅치 않아서 로고와 폰트를 따로 떠와서 1개의 logo container에다가 두 가지 이미지를 넣은 후 하나의 container를 head.container의 요소로 구분.

-media query는 inner class를 제작한 후 원하는 요소들은 전부 inner class를 상속시키는 방법을 활용, 980px로 만들어서 모바일 기준 해상도에도 잘 나오게끔 설정.

<br>

![image](https://user-images.githubusercontent.com/84431962/130308609-14b518e5-b8fd-4744-a17d-c91cf29c0594.png)

-코로나 확진자 이동 경로 조회 시 날짜를 select box를 사용해서 원하는 날짜를 입력할 수 있도록 설정. 차후 js를 적용시켜 돋보기를 누르는 경우 그에 맞춰서 원하는 날짜가 조회될 수 있도록 만들기.

-지도의 출처;네이버지도
 
 <br>

 ![제목 없음](https://user-images.githubusercontent.com/84431962/131317330-eb320f39-30cf-477a-87c6-929e960bcc9f.png)
 
-원하는 날짜를 스크롤박스에서 선택해서 우측의 돋보기 아이콘을 클릭하면 사용자가 입력한 시간에 맞춰서 그 날짜에 있던 확진자들을 지도에 보여주는 시스템. 

-카카오맵 무료 API를 사용하였음.

-JS를 사용해서 지도와 확진자 검색 기능을 구현하였음. 카카오맵 무료 API를 사용해서 지도를 구현하였고 확진자 위치는 마커로 표시.

-확진자 list를 만들고 각 확진자의 정보를 가진 확진자 객체를 list에다가 push해서 확진자 data를 쌓아가는 방식. 만약 확진자 수가 엄청 많다면 이러한 식으로 저장하는 것이 불가능할 것이다. 차후 데이터베이스 등을 배우고 난 다음 이러한 방식을 구현하지는 못하더라도 어떤 식으로 해결해야 될 지에 대해서 생각해볼 것.


 <br><br>
 
<h3>Feedback></h3>


<h4>2021.08.21)</h4> 
-CSS와 HTML만을 사용해서 우선적인 Layout만 따놓은 상태. JS를 통해서 지도 내부에서 원하는 시간을 설정하는 경우 그에 맞춰서 확진자 이동 경로가 조회되는 것 구현하기.

-현재 모바일에서 "데스크탑으로 보기" 를 사용하지 않는 경우 글자가 전부 깨지는 상황. 추후 반응형에 대해 조금 더 공부하고 그 부분도 맞춰볼 것.

-나중에 서버를 공부하게 된다면 독자적인 도메인을 만들어서 독자적인 도메인에다가 서비스를 직접 해보고, 서비스 함에 있어서 불편한 점들을 찾아볼 것.

-현재 style.css의 각 클래스 이름이 조금 통일되지 않은 느낌이 적잖게 있음. 코드의 가시성을 위해서 이 부분도 나중에 수정할 것.

-현재 우측 상단의 COVID19(질병관리청) 배너만 클릭 시 blank 가 설정되어 있지 않음. 이 부분도 차후에 수정할 것.
<br>
<h4>2021.08.30)</h4>
-JS를 사용해서 지도와 확진자 검색 기능을 구현하였음. 카카오맵 무료 API를 사용해서 지도를 구현하였고 확진자 위치는 마커로 표시.

-확진자 list를 만들고 각 확진자의 정보를 가진 확진자 객체를 list에다가 push해서 확진자 data를 쌓아가는 방식. 만약 확진자 수가 엄청 많다면 이러한 식으로 저장하는 것이 불가능할 것이다. 차후 데이터베이스 등을 배우고 난 다음 이러한 방식을 구현하지는 못하더라도 어떤 식으로 해결해야 될 지에 대해서 생각해볼 것.

-검색을 새로 시도할 때 마다 마커가 지워지고 다시 생성된다면 각 날짜에 맞춰서 그 날짜에 해당하는 확진자만 나오기 때문에, 그러한 디테일도 수정할 것.

<h4>2021.08.31)</h4>
-에브리타임에 게시 및 런칭 완료. 아래 피드백들은 사용자에게 받은 피드백들을 정리한 것임.

-모바일 환경에서 보았을 때는 폰트 등이 깨져서 보이는 문제점이 있음 -> 현재 media quary를 사용해서 min-width를 980px로 설정해두어서, 모바일에서 '데스크톱으로 보기' 기능을 사용한다면 깨지지 않지만 그 외 환경에서는 폰트가 깨지는 등의 문제가 있음. 해결하기 위해선 모바일 전용 웹사이트를 새로 개발하는 것이 가장 확실하면서 정확한 해결 방안인데, 프론트 분야를 주력으로 하거나 하지 않기 때문에 이 부분에 대해서는 다른 방법으로 해결할 수 있다면 해결을 시도해보고 어쩔 수 없다면 시간을 활용해서 모바일 전용 사이트를 개발해 보도록 할 것.

-날짜를 스크롤식으로 사용하면 원하는 날짜를 선택할 수 있지만, 오늘, 어제, 그저께 등의 최근 3일정도를 한번에 조회할 수 있는 버튼이 있으면 좋을 것 같음. -> 3개의 버튼 추가 완료.

-최근 확진 리스트를 가장 최근 한 사례만 사용하지 말고, 최근 사례 2~3개 정도를 게시한다면 가장 최근 뿐만 아니라 근래의 확진자 동향을 알 수 있어서 더욱 좋을 것 같음. -> 가장 최근 2개 게시물이 나오도록 추가 완료.

-확진자의 이동 동선이 지도에 표시 되었으면 좋겠음 ->현재 지도를 카카오맵 API를 차용해서 사용하고 있기 때문에, 이 점은 카카오맵 API 내에서 기능을 찾아보고, 최대한 비슷한 기능을 잘 활용할 수 있도록 할것.
 
-선택한 날짜에 확진자가 없는 경우 확진자가 없다는 것을 보여주기 위해서 별도의 조건문을 추가.

<h4>2021.09.01)</h4>
-아래 피드백들은 사용자에게 받은 피드백들을 정리한 것임.

-오늘, 어제, 그저께 아이콘 css 파일 수정 -> 우선 button 클래스를 따로 정의해서 css 스타일 정리 완료.

-JS로 웹 크롤링을 구현하는 것이 그렇게 어렵지 않으니, 크롤링을 사용해서 정보를 조금 더 쉽게 받아올 수 있도록 해볼 것.

-스크롤바의 Default 값을 오늘 날짜로 설정한다면 사용함에 있어 더욱 편리할 것 같음 -> 해결 완료. (아래 피드백 참고)

<h4>2021.09.02)</h4>
-사이트를 처음 로딩 하였을 때 나오는 날짜의 default를 오늘 날짜로 나오도록 수정 완료.

-추가로 "오늘 어제 그저께" 버튼이 눌렸을 때 날짜의 default를 각 날짜에 맞는 값으로 변하도록 수정 완료.

<h4>2021.09.08)</h4>
-사이트를 처음 로딩 하였을 때 오늘의 날짜에 맞추어 마커가 생성 되도록 추가 완료.

<h4>2021.10.28)</h4>
-IOS 사파리에서 총무팀 전화번호가 깨지는 현상 발견 -> IOS에서 자동으로 전화번호에 태그를 걸어버려서 그럼. meta태그 한줄 추가로 해결.
 <br><br>
 
<h3>Contact></h3>

아주대학교 미디어학과 이동환 wkazxf@ajou.ac.kr 

아주대학교 미디어학과 김규래 kamgyul123@ajou.ac.kr

<h3>Contribution></h3>

아주대학교 사이버보안학과 류정식 xvbc@ajou.ac.kr
