# Feed

<img src="https://user-images.githubusercontent.com/86224851/153854878-c3bf1134-43b6-46c0-9af9-922adb73a755.gif">

이 예제는 트위터에 피드를 올렸을 때를 가정하여 웹 페이지를 제작해 본 것 이다.  
크게 header, content, footer...3개로 나눠 볼 수 있을 것 같다.  
header에는

1. 프로필 이미지
2. 닉네임
3. 피드 경과 시간
4. 팔로우 여부

content에는

1. 피드 내용

footer에는

1. 좋아요 개수
2. 댓글 개수
3. 댓글 작성창
4. 댓글 등록 버튼

세부적으로는 위처럼 나눌 수 있겠다.

header부터 살펴보도록하겠다.  
프로필 이미지는 클릭시 프로필 페이지로 이동해야하므로 **img** 태그를 **a** 태그로 감싸주었다.  
닉네임 또한 같은 기능을 해야하고, 작성자를 보여주는, 피드의 제목과 같은 부분이므로 **h1** 태그를 사용, **a** 태그로 감싸주었다.  
피드 경과 시간은 내용을 꾸며주기 쉽게 **span** 태그를 사용했다.  
팔로우 여부를 보여주는 버튼은 누르면 팔로우가 설정, 해제가 전환되므로 **button** 태그를 사용했다. **type**은 딱히 제출하거나 리셋하는 것이 아니므로 **button**으로 지정했다. 이 부분은 실제로 현업에서 작성하게 된다면, 사용자의 팔로우 정보가 변경되는 것이므로 **submit**으로 사용될 것 같기도 하다...

content 부분은 간단하다.  
피드 내용을 작성했으므로 **p** 태그를 사용했다.

footer 부분을 살펴보자.  
좋아요 개수와 댓글 개수는 클릭하면 텍스트가 변경되는 동작을 하거나, 입력창을 보여주는 동작을 하므로 **button** 태그를 사용해서 표현했다.  
댓글 작성창은 **textarea**를 사용해서 긴 텍스트도 입력할 수 있게 만들었으며, 댓글 등록 기능을 하는 **button**과 함께 사용되므로 **form** 태그로 감싸주었다.

```html
<body>
  <div class="feed">
    <div class="feed-user-profile">
      <a href="#"
        ><img
          src="https://user-images.githubusercontent.com/19285811/69063907-43da4800-0a58-11ea-8efb-4b57dca4e3fe.png"
          alt="user profile image"
      /></a>
      <div>
        <h1><a href="#">Kimbug</a></h1>
        <span aria-label="Posted 30 minutes ago">30 min</span>
      </div>
      <button type="button">Follow</button>
    </div>
    <div class="feed-content">
      <p>
        The most beautiful experience we can have is the mysterious. It is the
        fundamental emotion that stands at the cradle of true art and true
        science. — Albert Einstein
      </p>
    </div>
    <div class="feed-footer">
      <button type="button">10 Likes</button>
      <button type="button">0 Comments</button>
    </div>
    <form action="" method="get" class="feed-comment">
      <textarea
        name=""
        id=""
        cols="30"
        rows="10"
        placeholder="Write a comment"
      ></textarea>
      <button type="submit">Submit</button>
    </form>
  </div>
  <script src="app.js"></script>
</body>
```

이번에 눈여겨 볼 점은 원하는 폼을 만드는데 큰 덩어리로 나눠서 작성했다는 것이다. 이전 예제에서도 다뤄왔는데, 이 예제만큼 명확하게 나뉘었던 적은 없었던 것 같다.
