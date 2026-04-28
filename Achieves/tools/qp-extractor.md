1. open qp pyq
2. open dev mode (f12)
3. remove all the extra elements
4. click on console and paste this
```
document.head.insertAdjacentHTML('beforeend', `<style>
  *, html, body { overflow:visible!important; height:auto!important; max-height:none!important; position:relative!important; }
  .sidebar, .header, .footer, .nav { display:none!important; }
</style>`);
```
