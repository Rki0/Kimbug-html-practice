# Instagram User Profile

<img width="1018" alt="스크린샷 2022-02-12 오전 11 40 34" src="https://user-images.githubusercontent.com/86224851/153693576-3d6b25fb-9ef8-4eee-8c34-3b89daff35d2.png">

이번 예제는 인스타그램 프로필을 따라 만들어보는 것이다.  
크게 6개로 나눌 수 있을 것 같다.

1. 유저 닉네임
2. post, followers, following 개수
3. 서브 네임
4. 자기 소개(텍스트)
5. 자기 소개(링크)
6. 프로필 이미지

1번은 프로필 전체를 대표하는 이름이므로 **h1** 태그를 사용한다.  
2번은 여러 데이터를 key와 value로 표현하므로, 이를 리스트로 표현하는 **dl** 태그를 사용하자. **dt**에는 key를, **dd**에는 value가 될 값을 입력한다.  
3번은 서브네임이므로 그냥 **p** 태그를 쓰는 것 보다 **h2** 같은 태그를 사용했다.  
4번은 자기 소개 글을 작성한 것이므로 **p** 태그를 사용했고,  
5번은 개인적으로 넣고싶은 링크를 넣은 것이므로 **a** 태그를 사용했다.  
굳이 4, 5번을 따로 작성한 것은 줄을 바꾸기 위함도 있고, **p** 태그 내부에 **a** 태그를 넣는 것보다 작성이 편한기 때문이기도 하다.  
6번은 프로필 이미지이므로 **img** 태그를 사용한다.

```html
<body>
  <div class="user-profile">
    <div class="user-profile-data">
      <h1>_kimbug</h1>
      <dl>
        <div>
          <dt>Posts</dt>
          <dd>112</dd>
        </div>
        <div>
          <dt>followers</dt>
          <dd>238</dd>
        </div>
        <div>
          <dt>following</dt>
          <dd>238</dd>
        </div>
      </dl>
      <h2>우현</h2>
      <p>
        김버그 #frontend #구독 #디지털노마드
        🇰🇷🇯🇵🇳🇿🇨🇦🇨🇳🇩🇪🇮🇹🇨🇿🇦🇹🇵🇾🇧🇷🇺🇸🇬🇧🇮🇳🇹🇭🇹🇼🇻🇳🇲🇾🇸🇬🚩
      </p>
      <a href="youtube.com/c/kimbug">youtube.com/c/kimbug</a>
    </div>
    <div class="user-profile-photo">
      <img
        src="https://avatars.githubusercontent.com/u/19285811?s=48&v=4"
        alt="프로필 사진"
      />
    </div>
  </div>
</body>
```

여기서 볼 것은 **img** 태그의 위치이다. 보통 **img** 태그를 맨 위에 쓸 것 같은데, 이번에는 html의 논리적 흐름, 내용의 흐름 상 이미지보다는 개인 프로필 정보가 더 중요하게 여겨져서 아래에 적은 것이다.  
이렇게 되면 스크린 리더기를 사용하시는 분들도 갑자기 사진이 읽히는 것보다 훨씬 더 이해가 쉽게 될 것이다.  
이미지의 위치는 CSS를 통해 조정해줬다.
