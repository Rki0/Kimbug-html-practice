# Google Search Result Item

<img width="711" alt="스크린샷 2022-02-11 오후 10 01 37" src="https://user-images.githubusercontent.com/86224851/153595969-1deadd6c-2c16-4069-9192-52cec1e1b16b.png">

이번 예제는 구글에서 검색을 했을 때 페이지에 결과로서 보여지는 다양한 검색 결과 링크들을 그대로 표현해본다.  
크게 3개로 나눠볼 수 있을 것 같다.

1. 메인 제목 링크
2. url 하위 항목 링크
3. 페이지 내용에 대한 부분

1번의 경우 메인 제목을 보여줌과 동시에 해당 페이지로 이동하는 기능을 해야하므로 **h1** 태그로 텍스트를 작성하고, **a** 태그를 내부에 감싸 url 링크를 연결한다.  
2번의 경우 url과 해당 페이지로의 경로를 간단하게 설명하고 클릭시 해당 페이지로 이동하는 기능을 하므로 **a** 태그를 사용해 텍스트 표현과 링크를 동시에 해결하였다.  
3번의 경우 페이지 내용에 대한 부분이므로 **p** 태그를 활용하여 텍스트를 작성했다.

```html
<body>
  <div class="google-search-result-item">
    <h1>
      <a href="https://www.w3schools.com/html/html5_semantic_elements.asp"
        >HTML5 Semantic Elements - W3Schools</a
      >
    </h1>
    <a href="https://www.w3schools.com/html/html5_semantic_elements.asp"
      >https://www.w3schools.com › html › html5_semantic_elements</a
    >
    <p>
      Oct 27, 2019 - Examples of non-<strong>semantic elements</strong>:
      &lt;div&gt; and &lt;span&gt; - Tells nothing about its content. ... HTML5
      <strong>semantic elements</strong> are supported in all modern browsers.
      ... So, on the Internet, you will find HTML pages with &lt;section&gt;
      elements containing ...
    </p>
  </div>
</body>
```

눈여겨 볼 점은 3번의 텍스트에서 &로 시작하는 이상한 문자들이 있다는 것인데, 이들은 html escape code로 html 문서 내에서 태그를 텍스트로 사용하고 싶을 때 사용하는 것이다.  
이를 통해 html이 태그가 아닌 텍스트로 인식하게 만들 수 있다.
