#makeHtmlElement
This is a tool that can make html element by using javascript chain method

###Example
```js
var test = html()
    .add('div', {className: 'container', data: { info: 'extraInformation' }})
        .contains('div', {className: 'header'})
            .contains('h5', {className: 'headerTitle', text: 'This is a header'}).end()
        .add('div', {className: 'content'})
            .contains('p', {text: 'This is the content'}).end()
        .end()
    .build();
```
will return:
```html
<div class="container" data-info="extraInformation">
    <div class="header">
        <h5 class="headerTitle">This is a header</h5>
    </div>
    <div class="content">
        <p>This is the content</p>
    </div>
</div>
```
###Usage
```js
.add(htmlTag, objectOfAttribute);      //add new html element
.contains(htmlTag, objectOfAttribute); //add child html element
.end()                                 //back to parent node
```

