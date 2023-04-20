# ![](https://drive.google.com/uc?id=10INx5_pkhMcYRdx_OO4rXNXxcsvPtBYq) Curl 基本指令介紹

<br>

<!--ts-->
## 目錄
* [簡介](#簡介)
* [上傳檔案](#上傳檔案)
* [下載檔案](#下載檔案)
* [設置cookie](#設置cookie)
* [發送GET請求](#發送GET請求)
* [發送POST請求](#發送POST請求)
* [參考資料](#參考資料)
<!--te-->

---
<br>

## 簡介.
Curl 是一種在Linux環境命令列介面下使用的工具，主要用來與Web伺服器進行互動，<br>
可以發送HTTP/HTTPS/FTP等協議的請求，並接收伺服器返回的資料。<br>
Curl 的語法簡潔、易於使用，是測試API或網站功能的常用工具之一。

Curl 的基本語法如下:
```css
curl [options] [URL]
```
- [options]是可選的參數，可以指定請求方法、請求標頭、請求主體、請求參數等。<br>
- [URL]是要請求的網址。<br>

---
<br>

## 上傳檔案
```css
curl -F 'file=@/path/to/file' http://example.com
```
上述命令會將 /path/to/file 檔案上傳到 example.com。<br>
可以使用 -F 或 --form 參數來指定表單數據，並使用 @ 標記要上傳的檔案。<br>

---
<br>

## 下載檔案
```css
curl -O http://example.com/file.zip
```
上述命令會下載 example.com 的 file.zip 檔案到當前目錄下，並使用原檔名。<br>
如果要指定下載檔案的名稱，可以使用 -o 或 --output 參數。<br>

---
<br>

## 設置cookie
```css
curl --cookie 'name=value' http://example.com
```
上述命令會向 example.com 發送一個 HTTP 請求，並設置 cookie 為 name=value。<br>
可以使用 -c 或 --cookie-jar 參數來設置 cookie 的儲存位置。<br>

---
<br>

## 發送GET請求
```css
curl http://example.com
```
上述命令會向 example.com 發送一個 HTTP GET 請求，並顯示服務器返回的內容。<br>
可以使用 -v 或 --verbose 參數來顯示請求的詳細信息。<br>

---
<br>

## 發送POST請求
```css
curl -X POST -d 'key1=value1&key2=value2' http://example.com
```
上述命令會向 example.com 發送一個 HTTP POST 請求，並帶有兩個參數 key1=value1 和 key2=value2。<br>
可以使用 -H 或 --header 參數來設置請求頭。<br>

如要在curl的POST請求中傳遞JSON數據，可以使用以下命令：<br>
```css
curl -X POST -H "Content-Type: application/json" -d '{"key1":"value1", "key2":"value2"}' http://example.com/api/endpoint
```
這個命令中，-H選項指定HTTP請求標頭，-d選項則指定POST請求的數據。<br>
Content-Type指定了請求數據的格式為JSON，-d參數中的內容就是JSON數據，<br>
http://example.com/api/endpoint則是POST請求的URL。<br>

---
<br>

## 參考資料
* [Linux Curl Command 指令與基本操作入門教學](https://blog.techbridge.cc/2019/02/01/linux-curl-command-tutorial/) <br>
---
<!--ts-->
#### [目錄 ↩](#目錄)
<!--te-->
