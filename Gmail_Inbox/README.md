# Gmail Inbox

<img src="https://user-images.githubusercontent.com/86224851/153863474-ef7f07fa-0f02-4003-8879-64165eba002a.gif">

이번 예제는 Gmail의 형태를 구성하는 방법을 알아보았다.  
리스트보다 **table**을 이용하여 만들었다는 점이 눈에 띈다.  
크게 2개로 나눌 수 있을 것 같다.

1. 버튼, 보낸 이, 제목, 보낸 시간(thead)
2. 버튼, 보낸 이, 제목, 보낸 시간(tbody)

1번은 사실 웹 페이지 상에서 보이게 만드려는 의도보다는 스크린 리더기를 사용하는 분들을 위해서, 개발자들의 보다 편한 코드 이해를 위해서 작성되었다.  
또한, **tbody**에서 작성될 내용의 가이드라인 col을 만들기 위함이기도 하다.  
따라서, **tr** 태그 안에 **th**를 4개 만들어서 이어질 코드의 제목을 만들어줬고, 이들은 각 열을 대표하므로 **scope** 속성을 이용해 그를 명시해줬다.

2번은 1번에서 명시한 내용을 보다 자세히 작성하는 부분이라고 볼 수 있겠다.  
우선, 읽지않은 메일과 읽은 메일을 구분하기 위해 두 개의 **tr** 태그를 사용하여 각각 만들었다.  
각 행에는 4개의 열이 생성되어야한다.  
첫 째 열에는 체크박스와 별 표시를 사용하여 특정 기능을 수행하는 버튼을 만들 것이다. 체크박스의 경우 **input** 태그를 이용하는데, 이는 CSS로 직접 꾸밀 수가 없으므로 **label** 태그를 **id, for**간 연결을 통해 활용한다.  
별 모양 버튼의 경우 **button** 태그를 쓴 뒤 CSS로 꾸며줄 수 있기 때문에 문제없다.  
둘 째 열에는 보낸 이의 이름을 적어줬다.  
셋 째 열에는 메일의 내용을 적는다. 클릭 시 메일 내용을 더 자세하게 보여주는 페이지로 이동하므로 **a** 태그를 사용하였고, 읽지 않은 메일의 경우 이를 강조하기 위해 **strong** 태그로 감싸주었다.  
읽은 메일은 강조할 필요가 없으므로 **span** 태그를 사용했다.  
제목 바로 뒤에 붙는 내용의 일부는 강조 표시가 들어가지 않기 때문에 **span**을 사용했다.
마지막 열에는 보낸 시간을 적어줬다.

```html
<body>
  <table class="inbox">
    <thead class="sr-only">
      <tr>
        <th scope="col">Actions</th>
        <th scope="col">Sender</th>
        <th scope="col">Title</th>
        <th scope="col">Timestamp</th>
      </tr>
    </thead>

    <tbody>
      <tr class="unread">
        <td>
          <div class="inbox-actions">
            <div class="inbox-checkbox">
              <input type="checkbox" name="" id="inbox-1" />
              <label for="inbox-1" class="sr-only">Select this email</label>
            </div>
            <button type="button" class="inbox-star">
              <span class="sr-only">Add to favorite</span>
            </button>
          </div>
        </td>
        <td>Goorm Edu</td>
        <td>
          <a href="#">
            <strong class="sr-only">Unread</strong>
            <strong> Rate your course: FRONTEND 101 WITH KIMBUG </strong>
            <span>
              - Woohyeon. How’s everything going? We want to hear your opnion
              on...
            </span>
          </a>
        </td>
        <td>3:34 PM</td>
      </tr>

      <tr class="read">
        <td>
          <div class="inbox-actions">
            <div class="inbox-checkbox">
              <input type="checkbox" name="" id="inbox-1" />
              <label for="inbox-1" class="sr-only">Select this email</label>
            </div>
            <button type="button" class="inbox-star">
              <span class="sr-only">Add to favorite</span>
            </button>
          </div>
        </td>
        <td>Goorm Edu</td>
        <td>
          <a href="#">
            <strong class="sr-only">read</strong>
            <span> Rate your course: FRONTEND 101 WITH KIMBUG </span>
            <span>
              - Woohyeon. How’s everything going? We want to hear your opnion
              on...
            </span>
          </a>
        </td>
        <td>3:34 PM</td>
      </tr>
    </tbody>
  </table>
  <script src="app.js"></script>
</body>
```

눈여겨 볼 점은 **thead** 부분이 웹 페이지 상에 보이지않는, 가이드라인으로만 사용될 수 있다는 것이다.  
별도의 클래스(sr-only)를 지정해 CSS로 숨기되, 스크린 리더기에는 읽힐 수 있도록 만든 것이다.  
처음 이 예제를 봤을 때는 **li**를 사용할 생각을 했었는데, **table**로 작성할 때가 훨씬 이해하기 쉬운 코드가 된 것이 신기했다.  
두 태그의 활용법 차이에 대한 공부가 되었다!
