# html & css 정리

## html 정리

> HTML\(HyperText Markup Language\)은 웹을 이루는 가장 기초적인 구성 요소입니다. HTML은 웹 콘텐츠의 의미와 구조를 정의할 때 사용합니다. HTML 말고도 웹 페이지의 외형과 표현을 서술하고\(CSS\), 기능과 동작을 서술하는\(JavaScript\) 기술도 있습니다.

[https://developer.mozilla.org/ko/docs/Web/HTML](https://developer.mozilla.org/ko/docs/Web/HTML)

여기서 웹을 만드는 도구들의 역할을 대략적으로 알 수 있다. html은 웹 콘텐츠의 의미와 구조를 정의할 때 사용하므로 '의미'와 '구조'이라는 키워드에 집중해서 html이 무엇인지 살펴보고, 대표적인 태그의 사용법을 정리하려고 한다.

### HTML의 정의

html은 프로그래밍 언어가 아니라 **컨텐츠의 구조를 정의**하는 마크업 언어이다.

### HTML 태그

* head 태그: head 태그는 웹 브라우저에 표시되지 않는다. HTML의 메타데이터를 담고 있기 때문이다. head 태그에는 이나 CSS의 링크, 다른 메타데이터 등을 포함한다.
  * : 이것은 데이터를 설명하는 데이터이다. 에서 자주 쓰이는 것을 살펴보면

    * 문서의 character 인코딩

      ```markup
      <meta charset="utf-8">
      ```

      크롬과 같은 브라우저에선느 자동으로 잘못된 인코딩을 고치지만, 다른 브라우저에서는 문자 인코딩과 관련해서 문제가 발생할 수 있으므로 인코딩을 utf-8로 설정하는 것이다.

    * name 속성

      메타 요소가 어떤 정보의 형태를 갖고 있는지 알려준다.

    * content 속성

      실제 메타데이터의 컨텐츠\(내용\)이다.

      이 두 가지 속성을 통해서 내 웹페이지의 관리자를 정리하고 머릿말을 요약하는데 사용할 수 있다.

      ```markup
      <meta name="author" content="Park Jaehyeong">
      <meta name="description" content="This documentation is for my HTML learning">
      ```

      페이지 컨텐츠 관련 키워드를 포함시키는 것은 검색엔진에서 이 페이지가 더 많이 표시 될 가능성이 생기게 할 수 있다. \(Searching Engine Optimization, SEO\) 그렇지만 많은  기능들이 더 이상 사용되지 않는다. 왜냐하면 키워드에 수백 개의 키워드를 채워서 스팸을 발송하는 악용 사례가 있기 떄문에 검색 엔진들이 무시를 하게 되었다.



            정리하자면, 메타데이터의 설명을 위한 용도!

  * favicon: 웹 페이지의 아이콘. 열린 페이지의 탭에서 볼 수 있다. 대부분의 브라우저에서는 .gif나 .png와 같은 포맷을 지원하지만 인터넷 익스플로러 6 이전에서는 ICO 포맷만 적용되므로 .ico 포멧의 파일을 저장하는 것이 안전하다.

    ```markup
    <link rel="shortcut icon" href="favicon.ico" type="image/x-icon">
    ```

  * HTML에 CSS와 JavaScript 적용하기

    &lt;link&gt;는 항상 문서의 head 부분에 위치한다. 두 가지 속성을 가지는데, rel="stylesheet"는 문서의 스타일 시트임을 나타내고 href=""는 스타일 시트 파일의 경로를 포함한다.

    ```markup
      <link rel="stylesheet" href="my-css-file.css">
    ```

    &lt;script&gt;는 head에 들어갈 필요가 없다. &lt;/body&gt; 태그 바로 앞, 문서 본문의 맨 끝에 넣는 것이 좋다.

    ```markup
      <script src="my-js-file.js"></script>
      <!--script에는 src를 쓰는 것 주의!-->
    ```

  * 문서의 기본 언어 설정

    페이지의 언어를 설정할 수 있다. html 태그에 추가하여 설정한다.

    ```markup
      <html lang="en-US">
      <html lang="ko">
    ```
*  &lt;a&gt;: 링크 만들기. href="" 속성 값에 웹 주소를 넣는데, 이때 http:// 또는 https:// 와 같은 프로토콜을 빼먹고 적는다면 원하는 페이지로 이동하지 않음. **주의**

## css 정리

