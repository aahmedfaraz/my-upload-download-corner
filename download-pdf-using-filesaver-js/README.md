# Download Static Files using Filesaver CDN

using simple HTML and Javascript with Filesaver CDN

```js
<script
  src='https://cdnjs.cloudflare.com/ajax/libs/FileSaver.js/2.0.0/FileSaver.min.js'
  integrity='sha512-csNcFYJniKjJxRWRV1R7fvnXrycHP6qDR21mgz1ZP55xY5d+aHLfo9/FcGDQLfn2IfngbAHd8LdfsagcCqgTcQ=='
  crossorigin='anonymous'
  referrerpolicy='no-referrer'
></script>
```

## Syntax Used

```js
button.addEventListener("click", () => {
  const xhr = new XMLHttpRequest();
  const url = "./location/for/the/sample.pdf";
  xhr.open("GET", url, true);
  xhr.responseType = "blob";
  xhr.onload = () => {
    const file = new Blob([xhr.response], {
      type: "application/pdf",
    });
    saveAs(file, "sampleFile.pdf");
  };
  xhr.send();
});
```
