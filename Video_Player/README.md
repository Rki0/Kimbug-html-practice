# Video Player

<img width="497" alt="스크린샷 2022-02-17 오후 9 08 10" src="https://user-images.githubusercontent.com/86224851/154478743-55d41170-c02c-49ac-8329-4004e0344871.png">

이번 예제는 비디오 영상을 만드는 것이다.  
크게 2개로 나눌 수 있을 것 같다.

1. 비디오 영상
2. 제목, 간단한 설명

1번의 경우, **video** 태그를 사용했다. 특정 브라우저에서 지원하지 않는 파일 형식이 있을 수 있으므로 **source** 태그를 사용해 비디오 파일을 적어줬다.  
2번의 경우, 영상을 대표하는 제목 부분은 **h1**, 간단한 설명을 적는 부분은 **p** 태그를 사용했다.

```html
<body>
  <div class="video-player">
    <div class="video-container">
      <video controls>
        <source src="./assets/kimbug-bjj.mov" type="video/mp4" />
        <source src="./assets/kimbug-bjj.mp4" type="video/mp4" />
      </video>
    </div>
    <div class="video-player-info">
      <h1>주짓수 4주차 롤링 영상</h1>
      <p>30초 만에 압살 실화인가</p>
    </div>
  </div>
</body>
```

눈여겨 볼 점은 **source** 태그의 **type** 속성이다. 반드시 적어줘야한다는 것을 잊지말자.  
추가로, **video** 태그에는 **controls** 속성을 추가해서 브라우저에 영상이 재생될 수 있도록 만들었다. 이게 없으면 영상을 재생할 수 없으니 주의하자!
