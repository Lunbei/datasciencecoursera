<!DOCTYPE html>
<html><head>
<meta http-equiv="content-type" content="text/html; charset=UTF-8">
  <title>Markdown Editor</title>
  <script src="HelloWorld_files/marked.js"></script>
  <script src="HelloWorld_files/highlight.js"></script>
  <script src="HelloWorld_files/codemirror.js"></script>
  <script src="HelloWorld_files/xml.js"></script>
  <script src="HelloWorld_files/markdown.js"></script>
  <script src="HelloWorld_files/gfm.js"></script>
  <script src="HelloWorld_files/javascript.js"></script>
  <script src="HelloWorld_files/rawinflate.js"></script>
  <script src="HelloWorld_files/rawdeflate.js"></script>
  <link rel="stylesheet" href="HelloWorld_files/codemirror.css">
  <link rel="stylesheet" href="HelloWorld_files/default.css">
  <style>
    .CodeMirror pre{
      line-height: 14px;
    }
    #in, .CodeMirror{
      position: fixed;
      top: 0;
      left: 0;
      bottom: 0;
      width: 50%;
      overflow: auto;
      font-size: 12px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.2);
    }
    .CodeMirror-scroll {
      height: 100%;
      min-height: 100%;
    }

    #out{
      position: fixed;
      top: 0;
      right: 0;
      left: 50%;
      bottom: 0;
      overflow: auto;
      padding: 10px;
      padding-left: 20px;
      color: #444;
      font-family:Georgia, Palatino, 'Palatino Linotype', Times, 'Times New Roman', serif;
      font-size: 16px;
      line-height: 1.5em
    }

    @media screen and (max-width: 1024px) {
      #in {
        display: none;
      }
      #out {
        left: 0;
        padding-left: 10px;
      }
    }

    .view #in {
      display: none;
    }
    .view #out {
      left: 0;
      padding-left: 10px;
    }

    a{ color: #0645ad; text-decoration:none;}
    a:visited{ color: #0b0080; }
    a:hover{ color: #06e; }
    a:active{ color:#faa700; }
    a:focus{ outline: thin dotted; }
    a:hover, a:active{ outline: 0; }

    p{margin:1em 0;}

    img{max-width:100%;}

    h1,h2,h3,h4,h5,h6{font-weight:normal;color:#111;line-height:1em;}
    h4,h5,h6{ font-weight: bold; }
    h1{ font-size:2.5em; }
    h2{ font-size:2em; border-bottom:1px solid silver; padding-bottom: 5px; }
    h3{ font-size:1.5em; }
    h4{ font-size:1.2em; }
    h5{ font-size:1em; }
    h6{ font-size:0.9em; }

    blockquote{color:#666666;margin:0;padding-left: 3em;border-left: 0.5em #EEE solid;}
    hr { display: block; height: 2px; border: 0; border-top: 1px solid #aaa;border-bottom: 1px solid #eee; margin: 1em 0; padding: 0; }

    pre, code{
      color: #000;
      font-family: monospace;
      font-size: 0.88em;
      border-radius:3px;
      background-color: #F8F8F8;
      border: 1px solid #CCC;
    }
    pre { white-space: pre; white-space: pre-wrap; word-wrap: break-word; padding: 5px;}
    pre code { border: 0px !important; background: transparent !important; line-height: 1.3em; }
    code { padding: 0 3px 0 3px; }
    sub, sup { font-size: 75%; line-height: 0; position: relative; vertical-align: baseline; }
    sup { top: -0.5em; }
    sub { bottom: -0.25em; }
    ul, ol { margin: 1em 0; padding: 0 0 0 2em; }
    li p:last-child { margin:0 }
    dd { margin: 0 0 0 2em; }
    img { border: 0; -ms-interpolation-mode: bicubic; vertical-align: middle; }
    table { border-collapse: collapse; border-spacing: 0; }
    td, th { vertical-align: top; padding: 4px 10px; border: 1px solid #bbb; }
    tr:nth-child(even) td, tr:nth-child(even) th { background: #eee; }
  </style>
</head>
<body>
  <div id="in"><form><textarea style="display: none;" id="code"># (GitHub-Flavored) Markdown Editor

Basic useful feature list:

 * Ctrl/Cmd + S to save the file
 * Drag and drop a file into here to load it
 * File contents are saved in the URL so you can share files


I'm no good at writing sample / filler text, so go write something yourself.

Look, a list!

 * foo
 * bar
 * baz

And here's some code!

```javascript
$(function(){
  $('div').html('I am a div.');
});
```

This is [on GitHub](https://github.com/jbt/markdown-editor) so let me know if I've b0rked it somewhere.


Props to Mr. Doob and his [code editor](http://mrdoob.com/projects/code-editor/), from which
the inspiration to this, and some handy implementation hints, came.

### Stuff used to make this:

 * [marked](https://github.com/chjj) for Markdown parsing
 * [CodeMirror](http://codemirror.net/) for the awesome syntax-highlighted editor
 * [highlight.js](http://softwaremaniacs.org/soft/highlight/en/) for syntax highlighting in output code blocks
 * [js-deflate](https://github.com/dankogai/js-deflate) for gzipping of data to make it fit in URLs
</textarea><div class="CodeMirror CodeMirror-wrap"><div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 5.8px; left: 216.8px;"><textarea autocapitalize="off" autocorrect="off" wrap="off" style="position: absolute; padding: 0px; width: 1px; height: 1em;">is a markdown file</textarea></div><div style="display: none;" class="CodeMirror-scrollbar"><div class="CodeMirror-scrollbar-inner"></div></div><div draggable="true" tabindex="-1" class="CodeMirror-scroll cm-s-default CodeMirror-focused"><div style="position: relative;"><div style="position: relative; top: 0px;"><div style="height: 799px;" class="CodeMirror-gutter"><div class="CodeMirror-gutter-text"><pre>1</pre></div></div><div class="CodeMirror-lines"><div style="position: relative; z-index: 0; outline: medium none; margin-left: 25px;"><div style="position: absolute; width: 100%; height: 0px; overflow: hidden; visibility: hidden;"><pre><span class="cm-header">##</span> <span class="cm-header">This</span> <span class="cm-header">is</span> <span class="cm-header">a</span> <span class="cm-header">markdown</span> <span class="cm-header">file</span><span>​</span></pre></div><pre style="top: 1px; left: 187px;" class="CodeMirror-cursor">&nbsp;</pre><pre style="visibility: hidden;" class="CodeMirror-cursor">&nbsp;</pre><div style="position: relative; z-index: -1; display: none;"><div style="position: absolute; left: 0px; top: 0px; right: 0px; height: 574px;" class="CodeMirror-selected"></div><div style="position: absolute; left: 0px; top: 574px; right: 612px; height: 14px;" class="CodeMirror-selected"></div></div><div style=""><pre><span class="cm-header">##</span> <span class="cm-header">This</span> <span class="cm-header">is</span> <span class="cm-header">a</span> <span class="cm-header">markdown</span> <span class="cm-header">file</span></pre></div></div></div></div></div></div></div></form></div>
  <div id="out"><h2>This is a markdown file</h2>
</div>

  <script>
    var URL = window.URL || window.webkitURL || window.mozURL || window.msURL;
    navigator.saveBlob = navigator.saveBlob || navigator.msSaveBlob || navigator.mozSaveBlob || navigator.webkitSaveBlob;
    window.saveAs = window.saveAs || window.webkitSaveAs || window.mozSaveAs || window.msSaveAs;

    // Because highlight.js is a bit awkward at times
    var languageOverrides = {
      js: 'javascript',
      html: 'xml'
    }

    marked.setOptions({
      highlight: function(code, lang){
        if(languageOverrides[lang]) lang = languageOverrides[lang];
        return hljs.LANGUAGES[lang] ? hljs.highlight(lang, code).value : code;
      }
    });

    function update(e){
      var val = e.getValue();

      setOutput(val);

      clearTimeout(hashto);
      hashto = setTimeout(updateHash, 1000);
    }

    function setOutput(val){
      val = val.replace(/<equation>((.*?\n)*?.*?)<\/equation>/ig, function(a, b){
        return '<img src="http://latex.codecogs.com/png.latex?' + encodeURIComponent(b) + '" />';
      });

      document.getElementById('out').innerHTML = marked(val);
    }

    var editor = CodeMirror.fromTextArea(document.getElementById('code'), {
      mode: 'gfm',
      lineNumbers: true,
      matchBrackets: true,
      lineWrapping: true,
      theme: 'default',
      onChange: update
    });

    document.addEventListener('drop', function(e){
      e.preventDefault();
      e.stopPropagation();

      var theFile = e.dataTransfer.files[0];
      var theReader = new FileReader();
      theReader.onload = function(e){
        editor.setValue(e.target.result);
      };

      theReader.readAsText(theFile);
    }, false);

    function save(){
      var code = editor.getValue();
      var blob = new Blob([code], { type: 'text/plain' });
      saveBlob(blob);
    }

    function saveBlob(blob){
      var name = "untitled.md";
      if(window.saveAs){
        window.saveAs(blob, name);
      }else if(navigator.saveBlob){
        navigator.saveBlob(blob, name);
      }else{
        url = URL.createObjectURL(blob);
        var link = document.createElement("a");
        link.setAttribute("href",url);
        link.setAttribute("download",name);
        var event = document.createEvent('MouseEvents');
        event.initMouseEvent('click', true, true, window, 1, 0, 0, 0, 0, false, false, false, false, 0, null);
        link.dispatchEvent(event);
      }
    }

    document.addEventListener('keydown', function(e){
      if(e.keyCode == 83 && (e.ctrlKey || e.metaKey)){
        e.preventDefault();
        save();
        return false;
      }
    })

    var hashto;

    function updateHash(){
      window.location.hash = btoa(RawDeflate.deflate(unescape(encodeURIComponent(editor.getValue()))))
    }

    if(window.location.hash){
      var h = window.location.hash.replace(/^#/, '');
      if(h.slice(0,5) == 'view:'){
        setOutput(decodeURIComponent(escape(RawDeflate.inflate(atob(h.slice(5))))));
        document.body.className = 'view';
      }else{
        editor.setValue(decodeURIComponent(escape(RawDeflate.inflate(atob(h)))))
        update(editor);
        editor.focus();
      }
    }else{
      update(editor);
      editor.focus();
    }

    var GoSquared = { acct: 'GSN-265185-D' };
  </script>
  <script src="HelloWorld_files/tracker.js" async=""></script>


</body></html>