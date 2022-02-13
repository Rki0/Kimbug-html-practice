# Github Dropdown Menu

<video src="
https://user-images.githubusercontent.com/86224851/153756681-b147edbd-02f6-4408-9c0d-cd69b1f0f519.mov"></video>

이 예제에서는 Github에서 프로필을 눌렀을 때 보여지는 Dropdown Menu를 만들어봤다.  
크게 두 개의 파트로 나눌 수 있다.

1. 프로필 이미지
2. Dropdown Menu

1번의 경우, 프로필 이미지를 클릭했을 때 Dropdown Menu가 보이도록 할 것이므로, 클릭 동작을 받을 수 있게 **button** 태그로 **img** 태그를 감싸줬다.  
2번에서 JS가 중요한 부분이지만 본 내용은 html 활용법에 대한 내용이므로 설명하지않겠다.  
위 영상을 보면 Dropdown Menu가 아래로 나열되는 리스트 형태를 보이는 것을 알 수 있다.  
딱히 순서가 중요하지 않으므로 **ul** 태그를 사용했다.  
다만, 메뉴의 맨 위 부분은 여러 개의 리스트가 아니라 하나의 링크로만 존재하고, 이 부분은 리스트를 대표하는 부분이라고 생각해서 **h3** 태그로 제목임을 알려주고, **a** 태그를 사용해줬다.

```html
<body>
  <div class="dropdown">
    <button type="button" aria-label="Open user menu" class="dropdown-button">
      <img
        src="https://avatars.githubusercontent.com/u/86224851?s=40&v=4"
        alt="user profile image"
      />
    </button>

    <div class="dropdown-menu">
      <h3>
        <a href="#">Signed in as <strong>rohjs</strong></a>
      </h3>
      <ul>
        <li><a href="#">Your profile</a></li>
        <li><a href="">Your repositories</a></li>
        <li><a href="">Your projects</a></li>
        <li><a href="">Your stars</a></li>
        <li><a href="">Your gists</a></li>
      </ul>

      <ul>
        <li><a href="#">Feature preview</a></li>
        <li><a href="">Help</a></li>
        <li><a href="">Settings</a></li>
        <li><a href="">Sign out</a></li>
      </ul>
    </div>
  </div>

  <script src="./app.js"></script>
</body>
```

눈여겨 볼 점은 **div** 태그정도이다.  
전체를 하나의 묶음으로 묶어서 연관성을 알려주고, Dropdown Menu 부분을 다시 **div**로 묶어서 개별적인 기능의 분류를 해주었다.
