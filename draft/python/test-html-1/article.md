# Test

```html
<!doctype html>
<html>
  <head>
    <title>Collaborative Editor</title>
  </head>
  <body>
     
    <script src="/bower_components/codemirror/lib/codemirror.js"></script>
    <link rel="stylesheet" href="/bower_components/codemirror/lib/codemirror.css">
    <script src="/bower_components/codemirror/mode/javascript/javascript.js"></script>
    <script src="/socket.io/socket.io.js"></script>
    <script src="/bower_components/jquery/dist/jquery.min.js"></script>
    
    <script>
        var myCodeMirror = CodeMirror.fromTextArea(document.getElementById("editor"), {
            lineNumbers: true,
            mode: "javascript"
        });
    </script>
  </body>
</html>
```

ok?