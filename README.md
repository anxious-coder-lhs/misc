# misc
for testing only, this js is fork from https://github.com/brix/crypto-js

Steps to generate this JS
1, npm install crypto-js
2, browserify node_modules/crypto-js/*.js -s CryptoJS > crypto-js.js
3, change the code below
   change 
   return decodeURIComponent(escape(Latin1.stringify(wordArray)));
   to
   return decodeURIComponent(Latin1.stringify(wordArray));
   
   change
   return Latin1.parse(unescape(encodeURIComponent(utf8Str)));
   to
   return Latin1.parse(decodeURI(encodeURIComponent(utf8Str)));

   or it will meet error in k6