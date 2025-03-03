# Laravel 11 Honeybadger 錯誤追蹤

引入 honeybadger-io 的 honeybadger-laravel 套件來擴增使用 Honeybadger 錯誤追蹤，例外狀況、正常運行時間和排程監控都集中在一個地方，為關心產品品質和客戶滿意的開發人員打造的應用程式健康狀況監視。

## 使用方式
- 把整個專案複製一份到你的電腦裡，這裡指的「內容」不是只有檔案，而是指所有整個專案的歷史紀錄、分支、標籤等內容都會複製一份下來。
```sh
$ git clone
```
- 將 __.env.example__ 檔案重新命名成 __.env__，如果應用程式金鑰沒有被設定的話，你的使用者 sessions 和其他加密的資料都是不安全的！
- 當你的專案中已經有 composer.lock，可以直接執行指令以讓 Composer 安裝 composer.lock 中指定的套件及版本。
```sh
$ composer install
```
- 產生 Laravel 要使用的一組 32 字元長度的隨機字串 APP_KEY 並存在 .env 內。
```sh
$ php artisan key:generate
```
- 執行 __Artisan__ 指令測試你的 Honeybadger 配置。
```sh
$ php artisan honeybadger:install {專案 API 金鑰}
```
- 在瀏覽器中輸入已定義的路由 URL 來訪問，例如：http://127.0.0.1:8000。
- 你可以經由 `/debug` 來進行錯誤例外觸發。

## 畫面截圖
![](https://i.imgur.com/etJAD5w.png)
> 觸發錯誤例外以中斷程式流程

![](https://i.imgur.com/ncOBbcR.png)
> 使用 Honeybadger 確認程式錯誤的偵測
