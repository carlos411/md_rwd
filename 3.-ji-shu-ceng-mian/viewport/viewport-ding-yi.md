# 3.2.1 Viewport 定義

## 結論

* 桌機：瀏覽器中頁面的可視區域。
* 手機：每個手機的 viewport 都不一樣\([例：iphone11 的 viewport 是 414 x 896](https://yesviz.com/devices/iphone-11/)\)，對我們網頁來設不太有意義，用不到，我們需要做的是將頁面寬度設定成等於設備寬；以及瞭解目前最小看到的 viewport 寬，還是有到 320。

## 原文說明

The viewport is the user's visible area of a web page.  
**\(viewport 是網頁中的可視區域\)**  
  
The viewport varies with the device, and will be smaller on a mobile phone than on a computer screen.  
**\(viewport 會因設備異，而且通常手機上的 viewport 大小會比一般桌上型電腦螢幕來得小。\)**  
  
Before tablets and mobile phones, web pages were designed only for computer screens, and it was common for web pages to have a static design and a fixed size.  
**\(在還沒有平板、智慧型手機之前，網頁都是針對電腦螢幕來設計，而且通常都是版型固定大小。\)**  
  
Then, when we started surfing the internet using tablets and mobile phones, fixed size web pages were too large to fit the viewport. To fix this, browsers on those devices scaled down the entire web page to fit the screen.  
**\(然而，在有了平板、智慧型手機之後，大家開始大量使用這些裝置來上網，然而，過去的固定式版型大小通常很大，無法容納於這些行動裝置，所以最快的解決方式，就是瀏覽器將這些網頁直接自動縮小，直到可以容納為止。\)**  
  
This was not perfect!! But a quick fix.  
**\(雖然這不是完美的做法，但是是一個最快的解決方式。\)**

