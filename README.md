<div align="center"><img src="https://github.com/lyingdragon/test/assets/4422798/2573a766-5c1f-499f-ab3e-9317d9724af9" width="100"></div>
<div align="center"><h1>Kkoma Chat</h1></div>
<div align="center">웹브라우저에서 실행하는 웹 검색 AI 챗봇</div>
<div align="center"><br>

![](https://img.shields.io/badge/build-passing-brightgreen)
![](https://img.shields.io/badge/hello-sweet_world-orange)
![](https://img.shields.io/github/stars/facebook?style=flat)
![](https://img.shields.io/npm/dw/remark)

</div>
<hr>

Kkoma Chat은 node.js로 만든 웹사이트 전용 챗봇입니다. [Baby Chat](#)에 영감을 받아, 실행 구조는 똑같지만 웹사이트에 쉽게 연동할 수 있도록 개선했습니다. 설정 파일 하나만 만들면 당장 웹사이트에 챗봇 창을 붙일 수 있습니다.

> [!TIP]
> Baby Chat과 함께 사용할 수도 있습니다.

## 설정하기

실행하기 전에 연결할 웹사이트를 지정해야 합니다. 루트에 server.yaml 파일을 만들고 아래 내용을 추가하세요.

```yaml
website_address: “연결할 웹사이트 URL"
```

## 실행하기

이제 지정한 웹사이트와 통신하는 챗봇을 로컬에서 실행합니다.

```sh
yarn start
```

챗봇 연동 프로세스와 설정 방법은 [공식 문서](https://docs.kkoma-chat.good-domain.com)에서 볼 수 있습니다.

## 기여하기
`contribute.md`을 참고해서 코드에 기여해 보세요.

## 챗봇 UI 붙이기

연결할 웹사이트에는 Kkoma Chat Bot UI를 만들어야 합니다. 웹사이트 각 페이지에 kkoma-chat-ui.js를 임포트하세요.
```html
<body>
…
<script src="https://cdn.jsxxx.net/xxx/kkoma-chat-ui.min.js"></script>
</body>
</코드>
챗봇 UI를 붙일 곳에 다음처럼 입력하세요.
<코드>
<body>
…
  <div class="container">
    <h1>Kkoma Chat</h1>
    <input id="chat-text" type="text" placeholder="무엇을 물어볼까요?">
    <div id="answer"></div>
  </div>
…
</body>
```
웹사이트를 실행하고 Kkoma Chat UI 입력 창에 “hello”를 입력하고 엔터를 누르세요. “hello”라는 응답이 출력되면 잘 연결된 것입니다.
