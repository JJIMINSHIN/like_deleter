# 자동 좋아요/좋아요 취소 스크립트

친구의 요청으로 제작된 JavaScript 스크립트입니다.
이 스크립트를 사용하면 특정 웹사이트에서 자동으로 좋아요를 누르거나 취소할 수 있습니다.

## 사용 방법

F12를 눌러 개발자 도구를 열고 Console 탭으로 이동하세요.

원하는 스크립트를 복사한 후 콘솔 창에 붙여넣고 실행하세요.

## 🔻 좋아요 취소 스크립트

아래 스크립트를 실행하면 20초 동안 자동으로 좋아요를 취소합니다.

``` javascript
let cnt = 0;

const intervalId = setInterval(() => {
    for (const d of document.querySelectorAll('button[data-testid="unlike"]')) {
        d.click();
        cnt++;
    }
    window.scrollTo(0, document.body.scrollHeight);
}, 1000);

setTimeout(() => {
    clearInterval(intervalId); // setInterval 중지
    console.log(cnt + "개의 좋아요가 삭제되었습니다.");
    console.log("스크립트 끝!");
}, 20000);
```

🔺 좋아요 누르기 스크립트
``` javascript
아래 스크립트를 실행하면 20초 동안 자동으로 좋아요를 누릅니다.

let cnt = 0;

const intervalId = setInterval(() => {
    for (const d of document.querySelectorAll('button[data-testid="like"]')) {
        d.click();
        cnt++;
    }
    window.scrollTo(0, document.body.scrollHeight);
}, 1000);

setTimeout(() => {
    clearInterval(intervalId); // setInterval 중지
    console.log(cnt + "개의 좋아요가 표시되었습니다.");
    console.log("스크립트 끝!");
}, 20000);
```

## ⚠️ 주의 사항

- 이 스크립트는 특정 웹사이트에서만 동작할 수 있으며, 사이트 구조가 변경되면 정상 작동하지 않을 수 있습니다.
- 참고용 스크립트이며, 이로 인한 모든 책임은 스크립트 실행자에게 있습니다.
- 자동화된 활동이 웹사이트의 정책을 위반할 가능성이 있으니, 사용 전에 정책을 확인하세요.


