### topbar
---
https://github.com/buunguyen/topbar

```
<script src="path/to/topbar.js"></script>
```

```js
$('#btnStartSimple').click(function(){
  topbar.show()
})
$('#btnStopSimple').click(function(){
  topbar.hide()
})

$('#btnStartAdvanced').click(function(){
  topbar.config({
    autoRun : false,
    barThickness : 5,
    barColors : {
      '0' : 'rgba(26, 188, 156, .7)',
      '.3' : 'rgba(41, 128, 185, .7)',
      '1.0' : 'rgba(231, 76, 60, .7)'
    },
    shadowBlur : 5,
    shadowColor : 'rgba(0, 0, 0, .5)'
  })
  topbar.show();
  (function step(){
    setTimeout(function(){
      if(topbar.progress('+.01') < 1)step()
    }, 16)
  })()
})

$('#btnStopAdvanced').click(function(){
  topbar.hide()
})
```

```
```

