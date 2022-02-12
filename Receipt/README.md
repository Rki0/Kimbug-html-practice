# Receipt

<img width="402" alt="스크린샷 2022-02-12 오후 1 05 27" src="https://user-images.githubusercontent.com/86224851/153695946-12e7536e-4274-48e3-958c-4b9af42a32b9.png">

이번 예제는 바코드가 있는 영수증 화면을 만드는 것이다.  
크게 8개로 나눌 수 있을 것 같다.

1. 큰 제목
2. 발행인
3. 매장 로고
4. 매장 이름
5. 바코드
6. 발행일
7. 메뉴 당 가격
8. 총 가격

1번의 경우 이 영수증을 대표하는 제목이므로 **h1** 태그를 사용한다.  
2번의 경우 발행인에 대한 간단한 설명이지만 중요한 내용이므로 1번의 **h1** 태그 안에 작성하여 **span** 태그로 감싸 텍스트를 꾸밀 수 있게 해주었다.  
3번의 경우 정보 전달에 중요하다고 판단되지않으므로 CSS로 추가하는 것으로 하겠다.  
4번의 경우 영수증이 발행된 가게를 대표하므로 **h2** 태그를 사용했다.  
5번의 경우 사용자가 가장 주요하게 사용하는 기능이므로 강조를 하기 위해 **strong** 태그를 통해 중요하다는 것을 알려준다.  
6번의 경우 단순 날짜 표시 텍스트이지만 꾸며주기 위해서 **span** 태그로 감싸주었다.  
7번의 경우 key와 value 형태로 메뉴와 가격을 알려주고 있으므로 **dl** 태그를 사용했다.  
8번의 경우 7번보다 위에 표시되는게 맞지만 사용자에게는 편하지만, 개발자 입장에서는 논리적인 코딩을 위해 총 금액을 아래에 쓰는게 맞아서 html 문서 상에서는 7번보다 뒤에 써줬다. 또한 **dl**을 따로 써줘서 웹 페이지 상 여백과 코드 상 강조 기능으로도 사용했다.

```html
  <body>
    <h1>
      Bill sharing Request
      <span>from kimbug</span>
    </h1>
    <div class="receipt">
      <h2>McDonald's</h2>
      <strong class="barcode">
        <img src="./assets/barcode.svg" alt="Barcode" />
      </strong>
      <span aria-label="Issued on June 24th, 20xx">24.06.20xx</span>
      <div>
        <dl>
          <div>
            <dt>
              Coke Light - 0.3<span aria-label="litter">L</span>
              <dd>
                &dollar;1.50
              </dd>
            </dt>
          </div>
          <div>
            <dt>
              Heineken Beer - 0.5<span aria-label="litter">L</span>
              <dd>
                &dollar;3.25
              </dd>
            </dt>
          </div>
          <div>
            <dt>
              Chicken McNuggets
              <dd>
                &dollar;21.00
              </dd>
            </dt>
          </div>
        </dl>

        <dl>
          <dt>
            In total
            <dd>
              <strong>
                &dollar;25.75
              </strong>
              </dd>
          </dt>
      </dl>
      </div>
    </div>
  </body>
```

이번에 눈여겨 볼 점은 **strong** 태그의 활용인 것 같다.  
텍스트를 두껍게 만들 때만 사용한다고 생각하지말고, 다른 개발자가 내 코드를 봤을 때 "아, 여기는 뭔가 비중있는 컨텐츠를 썼나보다"라고 생각하며 이해하기 쉽게끔 만들 때도 사용한다는 것을 기억하자!  
추가적으로 L(리터)단위 같은 경우 스크린 리더기는 알파벳 L로 읽어버리기 때문에 **aria-label**을 사용해서 더 명확하게 설명해주었다는 것도 유저 친화적인 코드를 만드는데 도움이 된다고 생각한다.
