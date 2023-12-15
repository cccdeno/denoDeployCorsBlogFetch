# Blog -- CORS 到 deno deploy 版

## deno deploy

* https://corsblogfetch.deno.dev/

## github

* https://cccdeno.github.io/denoDeployCorsBlogFetch/public/index.html

## 關鍵

```js
// ...
let corsOrigin = '*'

app.use(
  oakCors({
    origin: corsOrigin,
    optionsSuccessStatus: 200, // some legacy browsers (IE11, various SmartTVs) choke on 204
  }),
)
console.info("CORS-enabled origin : ", corsOrigin);
// ...
```