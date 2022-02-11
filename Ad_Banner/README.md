# Ad Banner

<img width="549" alt="스크린샷 2022-02-11 오후 9 35 10" src="https://user-images.githubusercontent.com/86224851/153592562-0384aafd-ffbe-4735-bbcb-ad75810636ca.png">

이번 예제는 모달(modal)창을 활용한 광고 배너이다.  
크게 3가지 부분으로 나눠 볼 수 있을 것 같다.

1. 배너를 대표하는, 관통하는 주제인 문장
2. 광고에 대한 간단한 내용 설명
3. 클릭하면 이동하는 버튼

1번의 경우 내용을 대표하므로 **h1** 태그를 사용했다.  
2번의 경우 부가적인 설명을 하는 부분이므로 **p** 태그를 활용하였다.  
3번의 경우 누르면 결제 페이지로 이동하므로 button 태그보다는 **a** 태그를 활용하여 링크를 연결하는 것이 좋아보인다.

```html
<body>
  <div class="modal">
    <h1>
      Unlimited downloads. <br />
      Our best content. <br />
      No attribution.
    </h1>
    <p>
      As low as $9/mo <br />
      Buy subscription or credit packs
    </p>
    <a href="#" target="_blank">Join pro</a>
  </div>
</body>
```

한번 더 볼만한 부분은 **a** 태그에서 **target** 속성을 **\_blank**로 사용해서 새로운 탭을 열어 페이지를 띄우게 했다는 점인 것 같다.
