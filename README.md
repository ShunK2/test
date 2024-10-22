## google chromeを開いて、右クリックして一番下の検証をクリック

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
