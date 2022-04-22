# Text to Speech 文字转语音

A project from [JavaScript 30 -23](https://youtu.be/saCpKH_xdgs)

## What I learned

1. 文字转语音的简化步骤
   ```js
   const msg = new SpeechSynthesisUtterance();
   msg.text = "hello";
   speechSynthesis.speak(msg);
   ```
2. 更改语言
   ```js
   // 接上
   let voices = speechSynthesis.getVoices();
   msg.text = "您好";
   msg.voice = voices.find((voice) => voice.lang === "zh-CN");
   speechSynthesis.speak(msg);
   ```
3. 设置`msg.rate`, `msg.pitch`可更改语音的速度和音高
4. `array.find()`只返回第一个符合条件的元素
5. 向回调函数传递参数可以使用`bind`, eg`ele.addEventListener('click',toggle.bind(null,false))` is the same as `ele.addEventListener('click',()=>toggle(false))` and `ele.addEventListener('click',function(){toggle(false)}`
6. global variable 既可以直接在 js 中使用，也可以在前面加上`window.`, 如 `window.speechSythesis` or just `speechSythesis`

## Reference

- [MDN - SpeechSythesisUtterance](https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesisUtterance)
