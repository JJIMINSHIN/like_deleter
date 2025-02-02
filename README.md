# like_deleter

좋아요 취소
----
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

좋아요 누르기
----
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
