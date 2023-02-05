微博点击头像到全是自己微博动态的个人主页 复制以下内容到浏览器控制台回车执行

```javascript
function deleteMessage() {
  // 下箭头
  let iDom = document.getElementsByClassName('woo-font woo-font--angleDown morepop_action_bk3Fq')[0];
  if (iDom) {
    iDom.click();
    setTimeout(() => {
    // 删除点击
      document.getElementsByClassName('woo-box-flex woo-box-alignCenter woo-pop-item-main')[6].click();
    }, 10)
    setTimeout(() => {
      // 确认删除框 确认点击
      document.getElementsByClassName('woo-button-wrap')[1].click();
      console.log(true)
      setTimeout(() => {
        // 重复执行
        deleteMessage()
      }, 100)
    }, 300)
  }
}
// 执行
deleteMessage()
//想要提速可以多执行几次 deleteMessage()
```
