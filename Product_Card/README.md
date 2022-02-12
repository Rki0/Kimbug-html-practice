# Product Card

<img width="339" alt="스크린샷 2022-02-12 오전 11 25 03" src="https://user-images.githubusercontent.com/86224851/153692983-bca7a1ba-b25c-42b7-b5b3-039aea2e18a2.png">

이번 예제는 상품을 보여주고, 부가적인 정보를 표시하는 것이다.  
크게 4개의 부분으로 나눌 수 있을 것 같다.

1. 상품 이미지
2. 저자
3. 제목, 이벤트 표시
4. 평점

1번의 경우 **img** 태그를 사용하여 책 표지를 보여주었고, 아래에 책 제목, 저자 등 설명이 따라 올 것이므로 **alt**에는 아무것도 입력하지 않는 것으로 한다.  
2번의 경우 html 코드만 보면 3번보다 아래에 있지만, 이는 CSS를 통해 변경할 수 있으므로 신경쓰지말자. 되도록 html 코드는 논리적인 흐름에 맞게 작성하는게 좋다!  
아무튼 2번은 저자를 알려주므로 상품에 있어 중요한 부분이다. 따라서 **strong** 태그로 감싸주었다.  
3번의 경우 책 제목은 상품을 대표하는 타이틀이므로 **h1** 태그를 사용했다. 바로 옆에 붙는 "오늘의 책" 표시는 따로 클릭해서 어떤 동작을 지원하는게 아니라, "이 책이 잘 팔려요~" 라고 강조하고 싶은 것이므로 **strong** 태그로 감싸주었다.  
4번의 경우 아이콘을 나열해서 평점을 표시해줬다. 색깔은 CSS로 조정한다.

```html
<body>
  <div class="product-card">
    <div class="product-card-image">
      <img
        src="https://user-images.githubusercontent.com/19285811/69318246-becd7980-0c77-11ea-8324-6c43e2de8cf2.png"
        alt=""
      />
    </div>
    <div class="product-card-title">
      <h1>혼자가 혼자에게</h1>
      <strong aria-label="오늘의 책 선정">오늘의 책</strong>
    </div>
    <strong aria-label="저자 이병률" class="product-card-author">이병률</strong>
    <strong aria-label="평점" class="product-card-review">
      <span aria-hidden="true">
        <i class="fas fa-star"></i>
        <i class="fas fa-star"></i>
        <i class="fas fa-star"></i>
        <i class="fas fa-star"></i>
        <i class="fas fa-star-half"></i>
      </span>
      9.4
    </strong>
  </div>
</body>
```

여기서 볼만한 점은 **aria-hidden** 속성이다. 이는 스크린 리더기가 이 부분을 읽을지말지를 알려준다. **true**를 값으로 입력하면 숨기겠다는 뜻이므로, 리더기가 읽지않고 넘어간다.  
별 모양 아이콘은 리더기가 읽어도 딱히 의미가 없으므로 읽지않도록 처리한 것이다.
