# Breadcrumb & Pagination

<img width="496" alt="스크린샷 2022-02-11 오후 11 28 05" src="https://user-images.githubusercontent.com/86224851/153609447-46b835ed-f2ea-4a2c-8aff-b95eaeee414e.png">

이번 예제는 **a** 태그가 연속적으로 나열되는 대표적인 형태에 대한 것이다.  
그 중 Breadcrumb라는 것은 **a** 태그들을 나열해서 해당 페이지로 이동할 수 있게 만든 것으로, 위 이미지에서 위에 있는 파트가 그 대표적인 예시이다.  
Pagination은 1,2,3...page 링크들의 종합을 말하며, 위 이미지에서 아래에 있는 파트가 대표적인 예시이다.

우선, Breadcrumb 부터 살펴보자. 매우 간단하다.  
맨 앞 이미지는 정보로서의 가치가 없다고 판단하여 CSS로 넣어줬고, 나머지는 클릭 시 해당 페이지(홈페이지, 파생 페이지)로 이동해야하므로 **a** 태그를 사용했다.  
두 **a** 태그 사이의 / 표시의 경우, 일반 텍스트로 작성한다면 CSS를 적용하기 귀찮아지므로 아예 CSS로 입력을 해줬다.

Pagination은 1,2,3...이렇게 페이지 번호가 계속해서 나열되는 구조를 가지므로, 순서가 있는 리스트로 표현하면 좋을 것 같다.  
따라서 **ol** 태그를 사용하였고, 각 **li** 태그 안에는 **a** 태그를 넣어서 해당 번호의 페이지로 이동할 수 있게 해줬다. **ol**은 직계 자식 요소로 **li**만을 받으므로 이 부분을 주의하자.  
한가운데 있는 ...은 따로 연결할 링크가 있는 것도 아니고, 그렇다고 ... 텍스트만 입력하는 것은 의미 전달이 잘 되지않으므로 **button** 태그를 활용했다. 다만, 사용자가 누르지 못하게 만들어야하므로 **disabled** 속성을 추가해서 비활성화 시켜줬다.

```html
<body>
  <div class="breadcrumb">
    <a href="https://github.com/rhojs" aria-label="Go to rohjs profile page"
      >rhojs</a
    >
    <a
      href="https://github.com/rhojs/bugless-101"
      aria-label="Go to bugless-101 repository page"
      >kimbug</a
    >
  </div>
  <div class="pagination">
    <a href="#" aria-label="Go to previous page" class="disabled">Previous</a>
    <ol>
      <li class="current-page">
        <a href="#" aria-label="Current page. Go to page 1">1</a>
      </li>
      <li>
        <a href="#" aria-label="Go to page 2">2</a>
      </li>
      <li>
        <a href="#" aria-label="Go to page 3">3</a>
      </li>
      <li>
        <a href="#" aria-label="Go to page 4">4</a>
      </li>
      <li>
        <a href="#" aria-label="Go to page 5">5</a>
      </li>
      <li>
        <button type="button" disabled>...</button>
      </li>
      <li>
        <a href="#" aria-label="Go to page 6">6</a>
      </li>
      <li>
        <a href="#" aria-label="Go to page 7">7</a>
      </li>
      <li>
        <a href="#" aria-label="Go to page 8">8</a>
      </li>
      <li>
        <a href="#" aria-label="Go to page 9">9</a>
      </li>
    </ol>
    <a href="#" aria-label="Go to next page">Next</a>
  </div>
</body>
```

눈여겨 볼 점은, **aria-label** 속성이다. 이는 스크린 리더기를 사용하시는 분들에게 도움이 되는 API로, 스크린 리더기가 **aria-label** 속성에 들어가 있는 값을 읽어준다. 따라서 우리 눈에 보이는 다양한 형태에 대한 어떤 설명을 적어 놓으면 몸이 불편하신 분들도 더욱 쉽게 웹을 사용할 수 있을 것이다.

추가로, 리스트 맨 앞의 Previous는 현재 페이지가 1페이지로 맨 앞에 있으니 비활성화 된 것으로 표시를 해줬는데, 나중에 가면 이를 CSS나 JS로 동적으로 적용되도록 해야하므로 이런 부분도 참고해놓으면 좋을 것 같다.
