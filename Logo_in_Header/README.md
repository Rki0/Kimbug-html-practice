# Logo In Header

<img width="1341" alt="스크린샷 2022-02-11 오후 11 13 49" src="https://user-images.githubusercontent.com/86224851/153607011-48aa262a-70e5-4ab0-97e5-10ccbd173e7f.png">

이번 예제는 웹 페이지 헤더 부분에 대표 로고와 메뉴를 만들어보는 것이다.  
크게 두 부분으로 나눌 수 있을 것 같다.

1. 웹 페이지 로고
2. 메뉴

헤더에 모두 함께 포함되는 것이므로 **div**로 요소들을 감싸주고 시작하자.  
1번은 로고이므로 **img** 태그를 사용하고, 클릭시 홈페이지를 보여주는 기능을 하므로 **a** 태그로 감싸준다.  
문제는 다른 개발자가 코드를 봤을 때 url들만 적혀있으니..이게 도대체 뭘 의미하는 것인지 한번에 알기가 어렵다.  
그래서 **h1** 태그로 이들을 감싸서 부가적인 설명을 적어놓을 수 있다. 다만, 그렇게되면 CSS로 텍스트를 가려주는 번거로움이 있어서 보통 **img** 태그의 **alt** 속성에 설명을 작성한다.  
2번은 Q&A 페이지를 보여주는 것이므로 **a** 태그를 사용하였고, & 텍스트를 사용하기 위해 html escape code를 써주었다.

```html
<body>
  <div class="header">
    <h1>
      <a href="./index4.html">
        <img
          src="https://statics.goorm.io/logo/edu/goorm_edu.svg"
          alt="Goorm Edu"
        />
      </a>
    </h1>
    <a href="https://edu.goorm.io/qna">Q&amp;A</a>
  </div>
</body>
```

**alt** 속성은 대체 텍스트로 쓰이는 것 뿐만이 아니라 이미지에 대한 설명으로 쓰일 수 있다는 것을 기억하자!
