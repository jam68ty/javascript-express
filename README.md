# JavaScript Express Demo

## 使用Express作為後端

### 建立專案、選擇架構

1. 建立一個專案命名為`javascript-express`
![](https://i.imgur.com/qTNeXvf.png)

2. 進到專案裡，在terminal安裝套件：`npx express-generator`
![](https://i.imgur.com/OStUizn.png)

3. 選擇模板：`express --view=pug .`
4. 執行`npm install`安裝相依套件
5. 執行`$env:DEBUG='javascript-express:*'; npm start`查看port是否listening(各環境語法不同：https://expressjs.com/en/starter/generator.html)

如果上述都成功的話，進入`http://localhost:3000`可以看到以下畫面
![](https://i.imgur.com/mBplFgr.png)

要停止的話只需要按ctrl+C
下次要再開啟的話也只需要輸入`npm start`就好
![](https://i.imgur.com/Gb9gse8.png)
> 等同於執行`node ./bin/www`


### 建立API

1. 在`javascript/routes/index.js`裡新增一個GET API
![](https://i.imgur.com/Rbp3KhR.png)
```javascript=
router.get('/api/sayHi', function(req, res, next) {
  res.send('hi');
});
```
2. 執行伺服器：`npm start`
![](https://i.imgur.com/TjcogXS.png)

3. 瀏覽器上右鍵-檢查，可以看到發出了一個GET的Http request
![](https://i.imgur.com/kPrOiUJ.png)

> 也可以使用線上工具[POSTMAN]([https://](https://universal-moon-12741.postman.co/workspace/My-Workspace~2bb1ccee-c481-4073-8c77-10c489644615/request/create?requestId=a5789b40-b739-4b67-bf5c-917bd0517c68))來測試(需要下載到本地才能對local端的伺服器發request)，他顯示的結果會與瀏覽器上看到的一樣：
> ![](https://i.imgur.com/NpVCn6X.png)
