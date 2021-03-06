# Documentation

不管是怎麼樣的文件，都對開發端非常有價值，業務端則不一定。撰寫文件與維護文件需要人力成本，在業務端的需求與壓力下，了解撰寫文件的優先權是非常重要的。

通常下面這些文件都會隨著原始碼進入版本控制系統。一來是為了要記錄修改歷程，另一個更重要的原因是，這些文件都是跟原始碼高度相關，因此進入版控可以讓文件能隨著原始碼保留下來，而不是成為一個*不成文的規定*。

以下介紹開發端應該有什麼樣的文件，與它的內容和存在的必要性，這將能幫助決定撰寫優先權。

## 產品概觀的介紹文件

一個好的產品（或函式庫，下面亦同），如果沒有好的介紹的話，就沒有人能了解它；無法了解，將會很難使用；使用上有困難，維護自然就不容易。

因此，產品**必須**要有一份介紹文件，來讓初次看到的人可以快速了解它能做什麼，以及為何而存在；**建議**也要介紹如何快速開始使用產品，有助於開發者了解產品最核心的功能。

**建議**介紹文件與快速使用可以寫在專案目錄下的 `README.md` 檔裡，因為大部分的版控管理介面都會自動開啟這份檔案，這也是可以符合上述需求：讓初次進到專案目錄的人可以快速了解狀況。而產品使用細節則**建議**放在專案目錄裡的 `docs/`目錄下。

## 環境文件

說明產品建置的環境需求，包括開發、測試與上線環境如何建置等。不管是資深人員或是新進人員，要維護一個產品，勢必會經過開發、測試與上線的流程。

因此，**必須**要有一份文件是說明該如何建置環境。此份文件除了對開發人員非常重要之外，也很適合提供給維運人員參考。

範例如下：

```markdown
## System Requirement

### Run time requirement

* Apache 2.4
* PHP 7.0.7+
* PHP Extensions
  + [cURL](http://php.net/manual/en/book.curl.php)
  + [OpenSSL](http://php.net/manual/en/book.openssl.php)

### Build time requirement

* Composer
* Node.js 6.1+
```

此份文件可以很清楚了解，執行環境（Run time）除了 Apache 與 PHP 7 外，還需要安裝 cURL 和 OpenSSL，同時也會知道建置時期的環境（Build time）需要 Composer 與 Node。

**建議**這份文件也可以寫在專案目錄下的 `README.md` 檔裡。

## 建置文件

大部分的軟體都是從原始檔轉換為可執行檔，通常稱為建置。該如何轉、產出物為何、以及如何佈署，**必須**要有一份文件說明，提供給開發人員參考使用。

範例如下：

```markdown
## Installation

Make sure you have `composer` and `npm` command:

    $ composer --version
    Composer version 1.2.2 2016-11-03 17:43:15
    $ npm -v
    3.10.8

If you don't, you can see [Composer][] and [Node.js][] official website for more information.

Run install command:

    # Install dependencies
    $ composer install
    $ npm install
    ...
    # Build front-end files
    $ ./node_modules/.bin/gulp
    
Finally, run PHP built-in server, and you can see `http://localhost:8080` on browser.

    $ php -S 0.0.0.0:8080 -t public

[Composer]: https://getcomposer.org/
[Node.js]: https://nodejs.org/
```

這份文件提供了完整的安裝與驗證方法。一開始會說明有哪些必要的工具，如果沒有的話可以去哪裡得到相關資訊，接著說明如何下安裝指令，最後則是說明如何驗證。

**建議**這份文件也可以寫在專案目錄下的 `README.md` 檔裡。

## 協作文件

專案會因為需求，而有不同的規範，如不同的 [workflow](/source-repository/workflow.md) 或 coding convention 。在這個前提下，**必須**要有一份文件說明此專案是採用何種 workflow 或 coding convention ，這樣才會方便讓其他人了解如何協作。

很明顯地，在新進成員到團隊時，這份文件將會非常重要；除此之外，有了這份文件，也會讓其他喜歡寫 code 的路人較有意願為這個專案付出。

**建議**這份文件可以寫在專案目錄下的 `CONTRIBUTING.md` 檔裡。

> 本專案也有一份 [`CONTRIBUTING.md`](/CONTRIBUTING.md) 可以參考。
