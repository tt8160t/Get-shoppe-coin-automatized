# 每天自動領取蝦幣(尚在改良中)
## 目的
- 希望能自動每天領取蝦幣，不需要使用者開機或者下指令，便自動領取蝦幣。
  (目前碰到的問題是，沒辦法在github action下執行，這部分的問題較難以解決，因為將網頁的html print出來後，跟原本的頁面呈現的都不太一樣)

## 使用到的套件及工具
### 套件       
- selenium
- time
- webdriver

### 工具
- vscode
- github


## 簡易流程
1. 透過selenium的方式開啟webdriver，並直接連接到"領取蝦幣"的登入後台網頁
(這部分要注意，每種首頁的登入帳號頁面有所差異，如果要領取蝦幣，記得是到領取蝦幣的後台，登入後才會轉到目標頁面)
2. 找出"帳號","密碼","登入"的class
3. 透過find找出目標class，並在上面填入帳號密碼，並且登入。
4. 登入後頁面會自動跳轉至"領取蝦幣"的頁面
5. 找出"領取"的css，並點擊就成功領取
6. 將上述程式上傳到github於固定時間自動啟動

## 流程中碰到的問題
(1) 目前出在簡易流程的3-4部之間，目前實際開啟頁面跑可以，但是透過github自動幫忙跑時，需要將頁面設成headless時，發現頁面沒有跳轉成功
