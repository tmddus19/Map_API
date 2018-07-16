# java script

- 변수를 선언할 땐 앞에 var을 붙여줘야된다.

-  `var a = 1;`을 하면 a에 1이 저장되서 a를 치면 1이나온다.

- `var arr = [];`으로 배열을 선언한다. (배열도 객체)

- arr.push(1)를 하면 배열에 1이 들어간다.

- arr.unshift : 값을 맨앞으로 넣어줌

- arr.pop : 맨뒷값 없애줌

- arr.shift : 맨앞값 없애줌

- `obj1.key = "value1";`

- obj1을 입력하면 `{key: "value1"}`이 나온다. 

- 아니면 `var obj1 = {key1: 'value1' }`이라고 쳐도 똑같은 값이 나온다.

- `var arr = [1,2,3,4,5];` 을 하고

- ```javascript
  for (var i=0; i<4; i++) {
       console.log(arr[i])
  }
  ```

​        하고나면 값이

- ```javascript
  1
  2
  3
  4
  이렇게 나온다.
  ```

  함수를 부를 땐 function name(arguments) {} 이런식으로 사용한다.

- `document.getElementById('query');` id가 query인것을 찾아준다.

- `document.getElementById('query').outerHTML = ('좋은 아침입니다!');`을 치면 검색창에 
  `"좋은 아침입니다!" `가 뜨고 없어지지 않는다.

-   

  ```javascript
  function sayHi() {
      alert('안녕 오랜만이야!')
  }
  ```

  `sayHi();`를 하면 `안녕 좋은아침이야! `가 나온다.

- `var all_a = document.getElementsByTagName('a');`

  ```javascript
  all_a;
  HTMLCollection(342) [a, a, a, a, a, a, a.al_favorite, a.al_jr, a.al_happybean, a.btn_arw._btn_arw.fold, a#ke_kbd_btn.btn_keyboard, a.spat.ico_info, a.btn_turnon, a.btn_turnoff.active, a.btn.btn_login, a.btn.btn_view, a.btn.btn_view, a, a, a.hisoff, a.funoff, a, a, a.hisoff, a.funoff, a, a, a.hisoff, a.funoff, a, a, a.hisoff, a.funoff, a, a, a.t@my@._star._myBtn, a.keyword, a.btn_delete.spat._del, a.ton._star._myBtn, a.keyword, a._delMode, a._keywordOff, a._acOff, a._delAll, a._delDone, a._delAll, a._keywordOff, a._acOff, a.btn_close._close, a, a.an_a.mn_mail, a.an_a.mn_cafe, a.an_a.mn_blog, a.an_a.mn_kin, a.an_a.mn_shopping, a.an_a.mn_checkout, a.an_a.mn_tvcast, a.an_a.mn_dic, a.an_a.mn_news, a.an_a.mn_stock, a.an_a.mn_land, a.an_a.mn_map, a.an_a.mn_movie, a.an_a.mn_music, a.an_a.mn_book, a.an_a.mn_comic, a#PM_ID_btnServiceMore.PM_CL_btnServiceMore.an_btn_more, a.ah_a, a.ah_a, a.ah_a, a.ah_a, a.ah_a, a.ah_a, a.ah_a, a.ah_a, a.ah_a, a.ah_a, a.ah_a, a.ah_a, a.ah_a, a.ah_a, a.ah_a, a.ah_a, a.ah_a, a.ah_a, a.ah_a, a.ah_a, a.ah_a, a.ah_ha, a.ah_tab_btn.ah_tab_on, a.ah_tab_btn, a.ah_a, a.ah_da, a.ah_a, a.ah_da, a.ah_a, a.ah_da, a.ah_a, a.ah_da, a.ah_a, …]
  ```

  란 값이 나온다.

- 이벤트 추가하기`search.addEventListener(이벤트명, 해당함수)`

  ex)search.addEventListener('mouseover', function()
        {alert("안녕!")});

- all_a  -> 모든 a tag, sayHi  ->  알림을 주는 함수

- a tag위에 마우스가 위치했을 때, 알림을 준다.

- `var obj1 = {key1: {new_key1: {last_key1: 'value1'}}};`- 

![1531704694758](C:\Users\student\AppData\Local\Temp\1531704694758.png)

# 네이버 map api사용하기

- 구글에 네이버 맵 api라고 검색하고 맨처음뜨는것으로 들어간다.
- c9에 workspace를 하나 만든다.
- `rails g controller map index`로 컨트롤러를 만들어준다.
- routes.rb에 root  'map#index'를 해준다.
- 네이버 맵 api에 있는 지도 WEB API 가이드를 index.erb파일에 복사 붙여넣기 해준다.(10만번호출까지는 무료)
- ![1531705761521](C:\Users\student\AppData\Local\Temp\1531705761521.png)

​       두가지를 index.erb파일에 복사 붙여넣기 해준다.

- 두번째줄은 java script이기 때문에 <script></script>안에 써주어야한다.

  ```ruby
  <div id="map" style="width:100%;height:400px;"></div>
  
  <script type="text/javascript" src="https://openapi.map.naver.com/openapi/v3/maps.js?clientId=FZpcFUXI8gbUymcmQJMG&submodules=geocoder"></script>
  <script>
      var map = new naver.maps.Map('map');
  </script>
  ```

- 네이버 맵 api 에서 javascript v3을누르고, 사이트바로가기를누른다. 그리고 시작하기를 누른다.

- Tutorials에서 지도생성및 기본 동작을 누른다.

- 밑으로 내리면 지도 이동하기가 있다.

![1531707014709](C:\Users\student\AppData\Local\Temp\1531707014709.png)

을 복사 붙여넣기 해준다.

- Tutorials에서 지도컨트롤을 누른다.
- ![1531707168581](C:\Users\student\AppData\Local\Temp\1531707168581.png)

​        도 복사 붙여넣기 해준다. 그러면 지도에 줌인 줌아웃컨트롤이 생긴다.

- ![1531707410984](C:\Users\student\AppData\Local\Temp\1531707410984.png)

​        에서

- ```ruby
  <script>
  
      var mapOptions = {
          scaleControl: false,
          logoControl: false,
          mapDataControl: false,
          zoomControl: true,
          zoomControlOptions: {
          style: naver.maps.ZoomControlStyle.SMALL,
          position: naver.maps.Position.RIGHT_BOTTOM
          }
      };
  
      var map = new naver.maps.Map('map', mapOptions);
      var jeju = new naver.maps.LatLng(33.3590628, 126.534361);
      map.setCenter(jeju); // 중심 좌표 이동
      map.setZoom(15);     // 줌 레벨 변경
  </script>
  ```

  를 해주면

  ![1531707477409](C:\Users\student\AppData\Local\Temp\1531707477409.png)

​       이렇게 바뀐다.

- Tutorials에서 마커를 누른다.

- ```ruby
  
      var map = new naver.maps.Map('map', mapOptions);
      var jeju = new naver.maps.LatLng(33.3590628, 126.534361);    
      var naveraddr = new naver.maps.LatLng(37.3595704, 127.105399);  <- 변경
      map.setCenter(naveraddr); // 중심 좌표 이동     <-추가
      map.setZoom(15);     // 줌 레벨 변경
      
      var marker = new naver.maps.Marker({      <-  추가
      position: naveraddr,                      <-  추가
      map: map                                  <-  추가
      });                                       <-  추가
  
  ```

  ![1531707901341](C:\Users\student\AppData\Local\Temp\1531707901341.png)

​       이렇게 바뀐다.

- 지도의 크기를 바꾸고 싶으면`<div id="map" style="width:100%;height:400px;"></div>`에서 %나 px를 바꿔준다. 

- Tutorials에서 정보창을 누른다.

- ```javascript
  var cityhall = new naver.maps.LatLng(37.5666805, 126.9784147);
  
  var contentString = [
      '<div class="iw_inner">',
      '   <h3>서울특별시청</h3>',
      '   <p>서울특별시 중구 태평로1가 31 | 서울특별시 중구 세종대로 110 서울특별시청<br>',
      '       <img src="./img/hi-seoul.jpg" width="55" height="55" alt="서울시청" class="thumb" /><br>',
      '       02-120 | 공공,사회기관 > 특별,광역시청<br>',
      '       <a href="http://www.seoul.go.kr" target="_blank">www.seoul.go.kr/</a>',
      '   </p>',
      '</div>'
  ].join('');                       <-배열안에 있는것을 합쳐준다.
  
  var marker3 = new naver.maps.Marker({
      map: map,
      position: cityhall
  });
  
  var infowindow = new naver.maps.InfoWindow({
      content: contentString
  });
  
  naver.maps.Event.addListener(marker3, "click", function(e) {
      if (infowindow.getMap()) {
          infowindow.close();
      } else {
          infowindow.open(map, marker3);
      }
  });
  ```

  Examples의 다수의 마커에 이벤트 핸들러 사용하기에서

  ```javascript
  function getClickHandler(seq) {
      return function(e) {
          var marker = markers[seq],
              infoWindow = infoWindows[seq];
  
          if (infoWindow.getMap()) {
              infoWindow.close();
          } else {
              infoWindow.open(map, marker);
          }
      }
  }
  ```

  

  index.erb파일을 바꿔준다.

  ```javascript
      var markers = [marker, marker2, marker3];                   <- 추가
      var infoWindows = [infowindow, infowindow2, infowindow3];   <- 추가
      
      naver.maps.Event.addListener(marker, "click", getClickHandler(0));  <-변경
  
      naver.maps.Event.addListener(marker2, "click", getClickHandler(1)); <-변경
   
      naver.maps.Event.addListener(marker3, "click", getClickHandler(2)); <-변경
     
      for (var i=0, ii=markers.length; i<ii; i++) {
          naver.maps.Event.addListener(markers[i], 'click', getClickHandler(i));
      }
  ```

  

- 이미지 아이콘 넣기

  ```
  var markerOptions = {
      position: position.destinationPoint(90, 15),
      map: map,
      icon: {
          url: HOME_PATH +'/img/example/sally.png',
          size: new naver.maps.Size(50, 52),
          origin: new naver.maps.Point(0, 0),
          anchor: new naver.maps.Point(25, 26)
      }
  };
  ```

  

home_path부분에 `https://navermaps.github.io/maps.js/docs`을 넣으면 된다.