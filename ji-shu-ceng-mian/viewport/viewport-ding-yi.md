# Viewport 定義

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

## 補充說明

`viewport`：指的是可視範圍。桌機版的瀏覽器，viewport 的寬度就等於瀏覽器的寬度。所以 viewport 通常是針對手機版的網頁在使用，指定 viewport 的 width 為設備寬度\(device-width\)；初始放大倍率\(`initial-scale`\)為1；是否要讓使用者可以用手指去縮放內容\(user-scalable\)。

**沒有指定 viewport 時的狀況，顯示了桌機版的網頁版本\(下圖出自於博客來官網\)：**

**有指定 viewport 的正確情況，顯示了行動版的網頁：**

