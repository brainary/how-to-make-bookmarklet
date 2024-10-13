How to make bookmarklets to enhance websites
============================================

These are just some personal notes on how to make bookmarklets.

Basic bookmarklet template
--------------------------
Just runs a `alert(1);` payload
```js
javascript:(        // So browser knows what to do
    ()=>{           // "arrow" function
        alert(1)    // Actual code
    }
)()                 // Run "arrow" function
```

### Compact:
```js
javascript:(()=>{alert(1)})()
```

### Works with:
- Chrome

---

Add a floating window to website (fixed)
----------------------------------------
```js
javascript:(
    ()=>{
        var box = document.createElement("div");
        box.style = "position:fixed;top:100px;left:100px;width:200px;height:200px;background:#f00;z-index:999;";
        document.body.appendChild(box)
    }
)()
```

### Compact:
```js
javascript:(()=>{var box = document.createElement("div");box.style = "position:fixed;top:100px;left:100px;width:200px;height:200px;background:#f00;z-index:999";document.body.appendChild(box)})()
```

### Works with:
- Chrome
