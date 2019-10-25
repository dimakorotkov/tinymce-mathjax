# TinyMCE MathJax Plugin

<span class="badge-patreon"><a href="https://www.patreon.com/dimakorotkov" title="Donate to this project using Patreon"><img src="https://img.shields.io/badge/patreon-donate-yellow.svg" alt="Patreon donate button" /></a></span>
<span><a href="https://buymeacoff.ee/NXR1ZkP" title="Donate to this project using Buy Me A Coffee" rel="nofollow"><img src="https://img.shields.io/badge/buy%20me%20a%20coffee-donate-yellow.svg" alt="Buy Me A Coffee donate button"></a></span>

This plugin using [MathJax](https://www.mathjax.org) library for rendering math font.

This plugin compatible with TinyMCE 5 and MathJax 3.

## Install

### NPM:
```
npm i @dimakorotkov/tinymce-mathjax --save
```

You can install mathjax and tinymce from npm
```
npm i mathjax --save
```
```
npm i tinymce --save
```



### Download

* [Latest build](https://github.com/dimakorotkov/tinymce-mathjax/archive/master.zip)

## Usage

### TinyMCE editor

Configure your TinyMCE init settings by adding `external_plugins` and usage of `mathjax`: 

```
tinymce.init({
  ...
  external_plugins: {'mathjax': '/your-path-to-plugin/@dimakorotkov/tinymce-mathjax/plugin.min.js'},
  toolbar: 'mathjax',
  mathjax: {
    lib: '/path-to-mathjax/es5/tex-mml-chtml.js', //required path to mathjax
    //symbols: {start: '\\(', end: '\\)'}, //optional: mathjax symbols
    //className: "math-tex", //optional: mathjax element class
    //configUrl: '/your-path-to-plugin/@dimakorotkov/tinymce-mathjax/config.js' //optional: mathjax config js
  }
});
```

### View

For displaing mathjax on web page you have to add [MathJax](https://www.mathjax.org) to the website itself.
It is recommended to include /your-path-to-plugin/@dimakorotkov/tinymce-mathjax/config.js

```
  <script src="/your-path-to-plugin/@dimakorotkov/tinymce-mathjax/config.js" type="text/javascript" charset="utf-8"></script>
  <script src="/path-to-mathjax/es5/tex-mml-chtml.js" type="text/javascript" charset="utf-8"></script>
```

You can add an optional param to config.js - class
```
  <script src="/your-path-to-plugin/@dimakorotkov/tinymce-mathjax/config.js?class=custom-mathjax-element-class" type="text/javascript" charset="utf-8"></script>
```

## License - MIT
