# 開発者ツールを利用した簡単プログラミング
## google chromeを開いて、右クリックして一番下の「検証」をクリック
![スクリーンショット 2024-10-22 125324](https://github.com/user-attachments/assets/144a0f2c-c6ee-41aa-8d13-9d6754166be7)
## 「コンソール」をクリックして、ソースコードを貼り付け
![スクリーンショット 2024-10-22 152414](https://github.com/user-attachments/assets/1e5d708d-c53c-4c1f-a35b-b5fe2cf96572)
## プログラミングのソースコード
(これをコピーしてconsoleに貼り付けてください)
```
document.body.onmousemove = function(e) {
  var d = document.createElement('div');
  d.style.cssText = `
    position:absolute;
    width:10px;height:10px;
    background:hsl(${e.clientX%360},100%,50%);
    border-radius:50%;
    left:${e.clientX}px;top:${e.clientY}px;
    pointer-events:none;
  `;
  document.body.appendChild(d);
  setTimeout(() => d.remove(), 1000);
};
```
## 最後にエンターを押すと実行され、マウスカーソルの軌道が虹色になります。
## ページをF5で更新したら、元に戻ります。
