# Feature Box

<img width="486" alt="스크린샷 2022-02-11 오후 11 00 45" src="https://user-images.githubusercontent.com/86224851/153604883-31609626-7c08-49a7-8885-172db617e40b.png">

이번 예제는 이미지와 텍스트를 섞어서 설명을 하는 Feature Box를 만드는 것이다.  
크게 3개로 나눌 수 있을 것 같다.

1. 이미지 부분
2. 내용을 대표하는 텍스트
3. 부가적인 설명

1번은 **img** 태그를 사용해서 이미지를 넣으면 된다. **img** 태그에는 **alt** 속성을 쓰는데, 여기서는 2번에서 자세한 설명이 나오므로 중복될 수 있어 **alt**를 비워놓았다.  
2번은 내용을 대표하는 텍스트이므로 **h1**을 사용했다.  
3번은 부가적인 설명이므로 **p** 태그를 사용했다.

```html
<body>
  <div class="feature-box no-image">
    <!-- <img
        src="https://wac-cdn.atlassian.com/dam/jcr:bc1f15f9-3b2e-4c30-9313-0ebd6175f18c/File%20Cabinet@2x.png?cdnVersion=676"
        alt=""
      /> -->
    <h1>Free unlimited private repositories</h1>
    <p>
      Free for small teams under 5 and priced to scale with Standard
      ($3/user/mo) or Premium ($6/user/mo) plans.
    </p>
  </div>
</body>
```

눈여겨 볼 점은 **img** 태그에 주석 처리가 되어 있는 부분이다. 이렇게 되면 이미지가 보이지 않을텐데 왜 이렇게 했을까?  
개발자에 따라서 이미지가 정보로서 가치가 있는가에 대한 관점이 다르기 때문에, 굳이 **img** 태그를 써서 표현할 필요가 없다고 생각되면 **CSS**로 이미지를 넣는다.
그럴 경우 **CSS**는 아래와 같다.

```css
/* For feature box without image */
.feature-box.no-image {
  padding-top: 196px;
  background-image: url("https://wac-cdn.atlassian.com/dam/jcr:bc1f15f9-3b2e-4c30-9313-0ebd6175f18c/File%20Cabinet@2x.png?cdnVersion=676");
  background-repeat: no-repeat;
  background-position: center 40px;
  background-size: auto 140px;
}
```
