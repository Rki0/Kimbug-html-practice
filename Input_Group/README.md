# Input Group

<img width="774" alt="스크린샷 2022-02-13 오후 11 51 36" src="https://user-images.githubusercontent.com/86224851/153758792-fae992cb-28f0-4754-a1d3-5e15cb19a52a.png">

이번 예제는 사용자에게서 정보를 입력받는 란을 만드는 것이다.  
이전 예제들에서도 자주 나왔던 형태라서 크게 어려운 부분이 없다.  
우선, 크게 3개로 나눌 수 있다.

1. 제목
2. 내용
3. 사용자 정보 입력칸, 버튼

1번의 경우, 내용을 대표하는 제목이므로 **h1** 태그를 사용했다.  
2번의 경우, 내용을 나열하므로 **p** 태그를 사용했다.  
3번의 경우, 정보를 입력받고 전송하는 버튼이므로 **form** 태그로 **input, button** 태그를 감싸주었다.

```html
<body>
  <div class="subscription">
    <h1>Manage Subscriptions</h1>
    <p>
      You can follow the discussion on @kimbug without to leave a comment. Cool,
      huh? <br />
      Just enter your email address in the form here below and you are all set
    </p>
    <form action="" method="get" class="input-group">
      <input type="email" placeholder="Your Email" />
      <button type="submit">Subscribe</button>
    </form>
  </div>
</body>
```

볼만한 점은 **button** 태그의 **type** 속성이 **submit**이라는 것이다.  
추가적으로 **form** 태그의 **method** 속성이 **get**인 것도 잊지말고 체크해야할 부분이다.
