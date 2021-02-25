# LAB - 14 [![made-with-Markdown](https://img.shields.io/badge/Made%20with-Markdown-1f425f.svg)](http://commonmark.org)

## ![cs](https://img.shields.io/github/license/AL0YSI0US/Lab-14) ![open-pr](https://img.shields.io/github/issues-pr-raw/AL0YSI0US/Lab-14) ![closed-pr](https://img.shields.io/github/issues-pr-closed/AL0YSI0US/Lab-14)

**Hello wanderer**, <img src="https://raw.githubusercontent.com/MartinHeinz/MartinHeinz/master/wave.gif" width="30px">

## Codefellows Guidance for Lab 14

1. do has much has you can

### 🎨 Designers

+ [Louis Lassegue](https://github.com/mrloulass)
+ [Aloysious](https://github.com/AL0YSI0US)

## C O L L A B O R A T I O N

T/A Ron help us understand the line of code.

````javascript
Cart.prototype.removeItem = function (item) {
  localStorage.removeItem(item);
};
````

## R E F L E C T I O N S

We took breaks, took turns driving and navigating.
We saw each others strengths and utilized them to work together well.
Aloysious knew how to google for different concepts and code.
Louis knew how to implement the code and understood the flow.

### L I N K S  &  R E S O U R C E S

[LabTutorial](https://codefellows.github.io/code-201-guide/curriculum/class-14/lab/) *class guide*

[CSS reset](https://meyerweb.com/eric/tools/css/reset/) *Meyers Reset*


[Storage.removeItem](https://developer.mozilla.org/en-US/docs/Web/API/Storage/removeItem)()

````javascript
storage.removeItem(keyName);
````

The following function creates three data items inside local storage, then removes the image data item.

````javascript
function populateStorage() {
  localStorage.setItem('bgcolor', 'red');
  localStorage.setItem('font', 'Helvetica');
  localStorage.setItem('image', 'myCat.png');

  localStorage.removeItem('image');
}
````

[DEMO CODE](https://mdn.github.io/dom-examples/web-storage/) = This code reflects a rendered webpage that allows you to change the color, font and images that appear when an item is selected. It is operating between a single HTML and bunch of JavaScript files.

````javascript
var htmlElem = document.querySelector('html');
var pElem = document.querySelector('p');
var imgElem = document.querySelector('img');

var bgcolorForm = document.getElementById('bgcolor');
var fontForm = document.getElementById('font');
var imageForm = document.getElementById('image');

if(!localStorage.getItem('bgcolor')) {
  populateStorage();
} else {
  setStyles();
}

function populateStorage() {
  localStorage.setItem('bgcolor', document.getElementById('bgcolor').value);
  localStorage.setItem('font', document.getElementById('font').value);
  localStorage.setItem('image', document.getElementById('image').value);

  setStyles();
}

function setStyles() {
  var currentColor = localStorage.getItem('bgcolor');
  var currentFont = localStorage.getItem('font');
  var currentImage = localStorage.getItem('image');

  document.getElementById('bgcolor').value = currentColor;
  document.getElementById('font').value = currentFont;
  document.getElementById('image').value = currentImage;

  htmlElem.style.backgroundColor = '#' + currentColor;
  pElem.style.fontFamily = currentFont;
  imgElem.setAttribute('src', currentImage);
}

bgcolorForm.onchange = populateStorage;
fontForm.onchange = populateStorage;
imageForm.onchange = populateStorage;
````
