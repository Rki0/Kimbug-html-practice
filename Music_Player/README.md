# Music Player

<img width="620" alt="스크린샷 2022-02-14 오후 10 57 17" src="https://user-images.githubusercontent.com/86224851/153877582-2cc0a3e0-a8cd-4075-9a49-9d1a02f5369d.png">

이번 예제는 음악 재생 프로그램의 플레이리스트를 만들어 보았다.  
크게 3개의 부분으로 볼 수 있을 것 같다.

1. 앨범 이미지
2. 제목, 가수
3. 음악 재생 시간

우선, 플레이 리스트의 경우 순서가 중요하기 때문에 **ol** 태그를 사용했다. **ol** 태그는 직계 자식 요소로 **li**만을 가질 수 있다는 점을 기억해내자.  
1번의 경우 **img** 태그를 사용했다. 만약 이미지를 클릭해서 상세 정보 페이지로 이동하게 만들고자 한다면 **a** 태그를 추가적으로 붙여줄 수 있을 것이다.  
2번의 경우 곡 제목은 **h1** 태그를 사용하여 대표적인 파트임을 명시하고, 텍스트를 꾸미기 편하게 **span** 태그로 감싸주었다.  
가수 또한 중요한 부분이므로 **strong** 태그를 사용하였다.  
3번의 경우 **span** 태그를 사용해 단순한 시간 표시 텍스트를 꾸밀 수 있게 만들었다.

```html
<body>
  <ol class="music-player">
    <li class="music-play-item">
      <img
        src="https://m.media-amazon.com/images/I/814Rp76DidL._SS500_.jpg"
        alt="러브 엑스 마키나"
        lang="ko"
        class="music-album-cover"
      />
      <div class="music-info">
        <div class="music-info-detail">
          <h1><span lang="ko">러브 엑스 마키나</span> Love Ex Machina</h1>
          <strong> MLSL (밀레니엄 살롱) </strong>
        </div>
        <span><span class="sr-only">Duration</span> 04:09</span>
        <audio src="./assets/music-1.mp3" class="music-audio"></audio>
      </div>
    </li>

    <li class="music-play-item">
      <img
        src="http://image.genie.co.kr/Y/IMAGE/IMG_ARTIST/080/660/591/80660591_1560403300605_1_600x600.JPG"
        alt="올라가"
        lang="ko"
        class="music-album-cover"
      />
      <div class="music-info">
        <div class="music-info-detail">
          <h1><span lang="ko">올라가</span></h1>
          <strong>권선홍</strong>
        </div>
        <span><span class="sr-only">Duration</span> 03:33</span>
        <audio
          src="./assets/html-practice_13-music-player_assets_music-2.mp3"
          class="music-audio"
        ></audio>
      </div>
    </li>
  </ol>
  <script src="app.js"></script>
</body>
```

눈여겨 볼 점은 앨범 커버 사진을 작성하기 위한 **img** 태그이다.  
**alt** 속성에 노래 제목을 작성했는데, 문제는 **html** 태그의 **lang** 속성이 en으로 설정되어있다는 것이다.  
따라서, 스크린 리더기에서 오류가 발생하는 것을 방지하기 위해서 **img** 태그의 **lang** 속성을 ko로 설정해줬다.
