# async-g-i-s

Async and new alternative for the [g-i-s](https://www.npmjs.com/package/g-i-s).

## Installation

`npm i async-g-i-s`

## Async/await Usage
```js
const gis = require('async-g-i-s');

(async () => {
  try {

    const results = await gis("akif");
    console.log(results.slice(0, 10));

  } catch (e) {
    console.error(e);
  }
})();
```
## Promise Usage
```js
const gis = require('async-g-i-s');

gis("akif").then(console.log).catch(console.error);
```


Output:
```js
[
  {
    url: 'https://m.media-amazon.com/images/M/MV5BMWQwM2M4NDMtOTI3Ni00NTMyLWI4YzktYTNkMjcyYmYzNzY4XkEyXkFqcGdeQXVyMTMyMTYxODIy._V1_.jpg',
    height: 1477,
    width: 1034,
    color: [ 48, 48, 48 ]
  },
  {
    url: 'https://upload.wikimedia.org/wikipedia/tr/c/ca/AkifDizi.jpg',
    height: 350,
    width: 350,
    color: [ 16, 16, 16 ]
  },
  {
    url: 'https://upload.wikimedia.org/wikipedia/commons/7/7b/Mehmet_%C3%82kif_Ersoy.png',
    height: 1908,
    width: 1656,
    color: [ 192, 192, 192 ]
  },
  {
    url: 'https://erdemyayinlari.com.tr/wp-content/uploads/2021/12/akif.png',
    height: 450,
    width: 300,
    color: [ 248, 248, 242 ]
  },
  {
    url: 'https://cdnuploads.aa.com.tr/uploads/Contents/2021/12/26/thumbs_b_c_8d154765bbfa0e823854bff84badecad.jpg?v\\u003d132249',      
    height: 486,
    width: 864,
    color: [ 152, 46, 56 ]
  },
  {
    url: 'https://img.kitapyurdu.com/v1/getImage/fn:11653825/wh:true/wi:500',
    height: 779,
    width: 500,
    color: [ 2, 8, 8 ]
  },
  {
    url: 'https://img.a.transfermarkt.technology/portrait/big/526642-1629104912.jpg?lm\\u003d1',
    height: 390,
    width: 300,
    color: [ 24, 18, 11 ]
  },
  {
    url: 'https://i.ytimg.com/vi/Ycm31r2SaPo/maxresdefault.jpg',
    height: 720,
    width: 1280,
    color: [ 50, 252, 172 ]
  }
]
```

You can add extra queries to URL, or you can also filter out results from specfied:
```js
gis("akif", {
  query: { safe: "on" },
  userAgent: 'Mozilla/5.0 (compatible; Googlebot/2.1; +http://www.google.com/bot.html)'
});
```
Example, this will not fetch NSFW results. And change user agent to Googlebot.