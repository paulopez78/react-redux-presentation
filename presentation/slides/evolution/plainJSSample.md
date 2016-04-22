## Plain JS with HTML (1995)

```javascript
if (document.all||document.getElementById){
  document.write('<font color="'+neonbasecolor+'">')

  for (m=0;m<message.length;m++)
    document.write('<span id="neonlight'+m+'">'+message.charAt(m)
    +'</span>')
    document.write('</font>')
}
else
  document.write(message)
```

[Live Example](http://www.theworldsworstwebsiteever.com/)
