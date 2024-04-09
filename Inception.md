## Namaste React Course by Akshay Saini
# _Chapter 01 - Inception_

## Q: What is `Emmet`?
A: `Emmet` is the essential toolkit for web-developers. It allows you to `type shortcuts` that are then expanded into full pieces of code for writing `HTML and CSS`, based on an abbreviation structure most developers already use that expands into full-fledged HTML markup and CSS rules.
### **i) HTML Expansion**: Emmet allows us to quickly generate HTML code by using abbreviations.
For instance, `div>ul>li.item$*3`
```
<div>
    <ul>
        <li class="item1"></li>
        <li class="item2"></li>
        <li class="item3"></li>
    </ul>
</div>
```
### **ii) CSS Abbreviations**: Emmet also supports expanding CSS abbreviations
For instance, `m10`
```
margin: 10px;
```
### iii) Nested Elements: We can use > to nest elements within each other. 
For instance, `ul>li*3` would generate an unordered list with three list items.
```
<ul>
    <li></li>
    <li></li>
    <li></li>
</ul>
```

### iv) Siblings: We can use + to create sibling elements. 
For instance, `div+p+bq` would create a div, followed by a p, and then a blockquote.
```
<div></div>
<p></p>
<blockquote></blockquote>
```

### v) Multiplication: We can use the * operator to create multiple elements. 
For instance, `ul>li*5` would generate an unordered list with five list items.
```
<ul>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
</ul>
```

### vi) Numbering: Use $ to indicate a number that should be incremented in each subsequent item. 
For instance, `ul>li.item$*3` would create list items with classes item1, item2, and item3.
```
<ul>
    <li class="item1"></li>
    <li class="item2"></li>
    <li class="item3"></li>
</ul>
```

### vii) Grouping: Parentheses can be used to group elements. 
For instance, `ul>(li.item$*2>a{Item $})*3` would generate a list with nested items and anchor tags.
```
<ul>
    <li class="item1">
        <a href="#">Item 1</a>
    </li>
    <li class="item2">
        <a href="#">Item 2</a>
    </li>
    <li class="item3">
        <a href="#">Item 3</a>
    </li>
</ul>
```


## Q: Difference between a `Library and Framework`?
A: A `library` is a collection of packages that perform specific operations whereas a `framework` contains the basic flow and architecture of an application. The major difference between them is the complexity. Libraries contain a number of methods that a developer can just call whenever they write code. React js is library and Angular is Framework.
The `framework` provides the flow of a software application and tells the developer what it needs and calls the code provided by the developer as required. If a `library` is used, the application calls the code from the library.

### Another answer
A: A `Library` is a collection of pre-written code that provides specific functionalities or features. It is designed to be reused across different projects to save development time and effort.
- **Control**: When using a library, the developer maintains more control over the overall structure and flow of the application. The developer decides when and how to use the library's components and functions.
- **Usage**: Libraries are generally used to solve specific tasks or provide utilities. They are often "called" by the developer's code to perform specific actions or computations.
- **Inversion of Control**: In a library, the developer controls the flow of the application. The library doesn't dictate the overall structure or architecture of the application.

For instance, React.js is a JavaScript library developed by Facebook.
React is primarily concerned with rendering UI components and managing their state and updates. It can be integrated into different project setups and combined with other libraries to create complete applications.

A `Framework` is a structured, pre-designed architecture that provides a foundation for building an entire application. It dictates the overall structure, flow, and design patterns of the application.
- **Control**: When using a framework, the developer gives up some control over the application's structure and flow. The framework enforces certain conventions and rules that the developer must follow.
- **Usage**: Frameworks are used to build entire applications. They provide a foundation and a set of tools to handle various aspects of application development, such as routing, database interactions, user authentication, etc.
- **Inversion of Control**: In a framework, control is often inverted, meaning the framework controls parts of the application's flow. Developers extend or customize the framework's components to build the application's logic.

For instance, Angular is a front-end framework developed by Google.
Angular is used for building dynamic and feature-rich web applications, particularly single-page applications (SPAs).



## Q: What is `CDN`? Why do we use it?
A: A `content delivery network (CDN)` refers to a geographically distributed group of servers that work together to provide fast delivery of Internet content.
The main use of a CDN is to deliver content through a network of servers in a secure and efficient way.


## Q: Why is `React known as React`?
A: `React` is named React because of its ability to `react to changes in data`.
React is called React because it was designed to be a declarative, efficient, and flexible JavaScript library for building user interfaces.
The name `React` was chosen because the library was designed to allow developers to "react" to changes in state and data within an application, and to update the user interface in a declarative and efficient manner.
`React` is a `JavaScript-based UI development library`. `Facebook` and an `open-source developer community` run it.


## Q: What is `crossorigin in script tag`?
A: The `crossorigin` attribute sets the mode of the request to an HTTP CORS Request. 
The purpose of crossorigin attribute is used to share the resources from one domain to another domain. Basically, it is used to handle the CORS request. It is used to handle the CORS request that checks whether it is safe to allow for sharing the resources from other domains.
### _Syntax_
```sh
<script crossorigin="anonymous|use-credentials">
```

## Q: What is difference between `React and ReactDOM`?
A: `React` is a JavaScript library for building User Interfaces whereas `ReactDOM` is also JavaScript library that allows `React to interact with the DOM`.
The react package contains `React.createElement()`, `React.Component`, `React.Children`, and other helpers related to elements and component classes. You can think of these as the isomorphic or universal helpers that you need to build components. The react-dom package contains `ReactDOM.render()`, and in react-dom/server we have server-side rendering support with `ReactDOMServer.renderToString()` and `ReactDOMServer.renderToStaticMarkup()`.


## Q: What is difference between `react.development.js` and `react.production.js` files via `CDN`?
A: `Development` is the stage of an application before it's made public while `production` is the term used for the same application when it's made `public`.
`Development build` is several times (maybe 3-5x) `slower` than the `production build`.


## Q: What is `async and defer`?
A: `Async` - The async attribute is a `boolean attribute`. The script is downloaded in `parallel(in the background)` to parsing the page, and `executed as soon` as it is available (do not block HTML DOM construction during downloading process) and don’t wait for anything.
### _Syntax_
```sh
<script src="demo_async.js" async></script>
```

`Defer` - The defer attribute is a `boolean attribute`. The script is downloaded in `parallel(in the background)` to parsing the page, and `executed after the page` has finished parsing(when browser finished DOM construction). The `defer attribute` tells the browser `not to wait for the script`. Instead, the browser will continue to process the HTML, build DOM.
### _Syntax_
```sh
<script src="demo_defer.js" defer></script>
```

Unless you're supporting ancient legacy systems, always add `type="module"` to all your script tags:
```sh
<script type="module" src="main.js"></script> and place the tag inside <head>
```
```sh
 <script defer nomodule> can be used as a legacy fallback.
```


As the name suggests, it allows you to import `modules`, which makes it easier to organize your code.
Enable `strict mode` by default. This makes your code run faster, and reports more runtime errors instead of silently ignoring them.
Execute your code only after the DOM has `initialized`, which makes DOM manipulation easier. Thanks to this, you won't need to listen to load/readystatechange/DOMContentLoaded events.
Prevent top level variables from implicitly polluting the global namespace.
Allow you to use top-level await in supported engines.
Load and parse your code `asynchronously`, which improves load performance.





