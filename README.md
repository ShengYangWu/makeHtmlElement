#makeHtmlElement
This is a tool that can make html element by using javascript chain method

###Example
```
var test = html()
    .add('div', {className: 'container', data: { info: 'extraInformation' }})
        .contains('div', {className: 'header'})
            .contains('h5', {className: 'headerTitle', text: 'This is a header'}).end()
        .and('div', {className: 'content'})
            .contains('p', {text: 'This is the content'}).end()
        .end()
    .build();
```
will return:
```
<div class="container" data-info="extraInformation">
    <div class="header">
        <h5 class="headerTitle">This is a header</h5>
    </div>
    <div class="content">
        <p>This is the content</p>
    </div>
</div>
```

