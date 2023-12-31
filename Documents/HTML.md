<link rel="stylesheet" type="text/css" href="../Assets/content.css">
<h1 class="custom-header">HTML</h1>

<h1 class="toc-header">Table of Contents</h1>
<ul>
    <li><a href="#introduction">Introduction</a></li>
    <li>
    <a href="#basic-html-page-structure">Basic HTML page Structure</a>
        <ul>
            <li><a href="#header-header">Header Tag</a></li>
            <li><a href="#main-content-main">Main Content</a>
                <ul>
                    <li><a href="#article-element-article">Article Tag</a></li>
                    <li><a href="#section-element-section">Section Element</a></li>
                </ul>
            </li>
            <li><a href="#footer-element-footer">Footer Tag</a></li>
        </ul>
    </li>
    <li><a href="#semantic-tags-in-action">Semantic tags in action</a></li>
    <li>
    <a href="#forms-and-validation">Forms and Validation</a>
    <ul>
        <li>
        <a href="#form-validation">Form Validation</a>
        </li>
    </ul>
    <li>
    <a href="#input-types">Input Types</a>
    </li>
    <li>
    <a href="#form-submission">Form Submission</a>
    <ul>
        <li><a href="#using-get-for-form-submission">Using GET for form submission</a></li>
        <li><a href="#using-post-for-form-submission">Using POST for form submission</a></li>
    </ul>
    </li>
    <li>
    <a href="#submit">Submit</a>
    <ul>
        <li><a href="#action-and-method">Action and Method</a></li>
    </ul>
    </li>
    <li>
    <a href="additional-resources">Additional Resources</a>
    </li>
    <li>
    <a href="#best-practices">Best Practices for writing HTML Documents</a>
    </li>
</ul>



# Introduction

* HTML is a markup language that was introduced in 1990.
* Its the most basic and fundamental language that helps build and display contents of a webpage.
* A list of all HTML tags and their documentation can be found [here](https://www.w3schools.com/tags/default.asp).
* Another HTML tag cheatsheet can be found [here](https://www.coursera.org/learn/the-full-stack/supplement/guED4/semantic-html-cheat-sheet).
* An HTML Page is a basic structure which consists of different components such as tags and elements.

## HTML:

* Stands for Hypertext Markup Language
    * Hypertext: Text which contains links to other elements.
    * Markup: Refers to tags and elements used within a document.
* Simply a text file with a specific structure. 
* This structure consists of differnet components such as tags and elements.
* Have the `.html` suffix.
* Whenever you go to a website, the first page that often gets returned is called _index.html_.
* If you want to learn how to tell the browser to show the webpage content, learn ___CSS___.

# Basic HTML Page Structure

```
<!DOCTYPE html>
<html>
    <head>
    </head>
    <body>
    </body>
</html>
```

* Other tags such as `<main></main>, <footer></footer>` etc. can be used to describe a typical HTML page.
* A normal website can look something like this:
```
<!DOCTYPE html>
    <head>
    </head>
    <body>
        <header>
        <!-- Contains the header of a page, e.g. Your company name: Apple -->
        </header>
        <main>
        <!-- Main content of the web page -->
        </main>
        <footer>
        <!-- Social media links, contact us, etc.  -->
        </footer>
    </body>
</html>
```
* As can be seen above, the `<body>` element has 3 main elements, `<header>`, `<main>`  and `<footer>`, as shown in <a href="#basic-html-page-structure"></a>.
* It is important to note that semantic elements are not limited to this structure. Elements can be nested inside each other if it accurately describes the content. 

## Header `<header>`

* Usually contains thing such as company logos and navigation links. 
* The main navigation section of a webpage can also be defined semantically, using `<nav>` tags.

| ![alt text](./Resources/HTML/basicHTMLPage.png) |
|:--:|
| *Webpage with `<header>`, `<main>` and `<footer` tags*| 
* The `<nav>` element is used after the `<header>` element(which is used for logos).
* An example for this:
```
<!DOCTYPE html>
    <head>
    </head>
    <body>
        <header>
            <nav>
                <ul>
                    <li><a href="#home">Home</a</li>
                    <li><a href="#about">About</a</li>
                    <li><a href="#contact">Contact</a</li>
                </ul>
            </nav>
        </header>
    </body>
</html>
```


## Main Content `<main>`

* The two key semantic elements for your main content are the following elements:
    * Article
    * Section

### Article Element `<article>`

* The HTML specification states that "According to the World Wide Web Consortium's website, the `<article>` element indicates content which represents a _complete_ or _self-contained_ composition in a document page application or site that is _independently distributable_. 
    * Imagine articles in a newspaper. There are many articles on a page and you can cut out the individual articles with scissors if you want to. The `<article>` element can be thought of in this way. Examples would be:
        * Forum Post
        * User Comment
        * Article
        * Blog post
        * Interactive widget
        * Or any other independent item of content
* You should place your `<article>` within your `<main>` element.
* Example of how an `<article>` element can be used:
    * Say you are developing a blog about some holiday. Its good practice to contain the blog content inside the `<article>` element since it's a complete self-contained composition on a web-page.
    ```
    <body>
        <header>
        </header>
        <main>
            <article>
                <h2>This is my heading</h2>
                <p>My paragraph is gonna start like this</p>
            </article>
        </main>
        <footer>
        </footer>
    </body>
    ```
    * The reason for doing it this way is that the `<main>` element semantically represents the main content of a page. Inside there can be multiple `<article>` elements for things such as blog post lists.

### Section Element `<section>`

* You can add `<section>` elements to individually define sections of the article.
    * Should contain heading elements, e.g. `<h1>`, `<h2>`, etc. to semantically describe the section. 
* Doesn't require the `<article>` element. It all depends on how you want to semantically describe the page.

## Footer Element `<footer>`

* The footer element contains additional links or other content.
* Its usually at the end of the document.



# Tags and Elements:

* Each HTML element, consists of an opening tag enclosed in angle brackets. 
    * To create a paragraph, you type `<p>`.
* Most elements are paired with a closing tag, which has a `/` after the left angle bracket.
    * The closing tag for paragraphs would be, `</p`.
* HTML tags usually have some content inside them. Example:
    ```
    <p>This is a paragraph</p>
    ```
    Would generate something like this:

    <p>This is a paragraph</p>
* HTML elements can also contain other elements.
    ```
    <p>This is a <i>paragraph</i></p>
    ```
    _index.html_:
    <p>This is a <i>paragraph</i></p>

    * `<i>` is the italics element.
* Elements can also be self-closing, where the do not require the closing tag. 
    ```
    <p>This is a <br>paragraph</p>
    ```
    _index.html_:
    <p>This is a <br>paragraph</p>
    
    * Another way to 'close' the self-closing tag is to type a `/` before the right-angled bracket. `<br/>`.
* The rules and structure for elements and tags are known as the HTML specifiction. The HTML specification is managed by the world wide web consortium or __w3c__. 
* Whenever the HTML specification changes, a new version of HTML is standardized.
* The current version is HTML5.


# Semantic Tags in Action

* The little lemon restaurant has asked me to add a new blog page to their website. This blog page can be found [here](../Projects/Little-Lemon-Restaurant/src/blog.html).

# Forms and Validation

* You will use HTML forms to capture user input.
* Capturing input is one thing, but the form also needs to ensure that the data is usable. Need to ensure that the user input is valid.

## Form Validation

* Form validation is a process that ensures that the data entered by the user in a form is valid and conforms to rules defined by the developer.
* There are two methods of form validation:
    * Client-side Validation:
        * Checks for errors as soon as they are typed into the form
        * Done by the web browser or by JavaScript code and provides the user with immediate feedback
        * This process starts by checking if a form has been filled out correctly
        * If there are no errors, the form will be submitted to the server for processing
        * If there are errors, an error messgae will alert the user of the invalid data and how to change it for successful submission
    * Server-size Validation:
        * Checks for errors in the data after the form has been submitted to the server
        * More secure because it prevents malicious users from tampering with your website's code and submitting invalid data to your server
        * When the form data is received by the webserver, the backend will validate the data before processing
        * This enables the server to run more complex checks such as validating the data against a database or validating the data against business requirements
* Most websites use both forms of validation to provide immediate feedback to users but also to protect against malicious data submission and to ensure data integrity
* HTML has several input types that can help with validation
```
<!-- For inputting email addresses -->
<input type="email"> 
<!-- Telephone numbers -->
<input type="tel">
<!-- Website urls like www.google.com -->
<input type="url">
<!-- Dates -->
<input type="date">
<!-- Time -->
<input type="time">
<!-- Numeric values -->
<input type="number">
<!-- Numeric values with a minimum and a maximum -->
<input type="range">
<!-- Color values -->
<input type="color">
```


# Input Types:

* A cheatsheet for the input types can be found [here](https://www.coursera.org/learn/the-full-stack/supplement/FXL7l/input-types).
* A file containing different examples of input types can be found [here](../Projects/Little-Lemon-Restaurant/examples/input-types.html).


# Form submission:

* This section explains form submission to servers.
* Forms send data as a part of the HTTP request to the server.
* There are two ways a form can send data to a webserver:
    * Using the `GET` method: 
    * Using the `POST` method
* The developer can specify which method to use with the <b>method</b> attribute of the form element.
* Example Form: [here](../Projects/Little-Lemon-Restaurant/examples/form.html).
* If a submit button doesn't exist on the form, the form is submitted to the same url.

## Using `GET` for form submission:

* When the `GET` method is used for form submission, the data of the form is sent as a part of the URL.
* This means that the user data is appended to the end of the URL in the browser navigation bar.
* The server receives the `GET` request and extracts the data from the form URL.
* While this is an easy way to submit data, it has 3 key problems:
    * The length of a URL is limited to around 2000 characters depending on the browser being used. Some web servers allow longer length URLs but this inconsistency and character length limit can lead to loss of data.
    * The length of a requested URL is also limited by servers. Popular web services software such as Apache, Nginx have a default limit of around 4096 characters.
    * Security. Since the data is included in the URL, the url is stored in the web browser history and possibly the request logs on the webserver. If transmitting personal information such as credit card details, it poses major privacy and security risks.


## Using `POST` for form submission:

* When the form is submitted using the `POST` method, the form data is inserted into the content of the HTTP request.
* When the submit button is pressed, it will send an HTTP `POST` request with the data contained in the body of the request.
* The `POST` method is more secure than `GET`.
* However, the data can still be read by a third party listening to the HTTP request.
* To secure this completely, HTTPS is used to encrypt the data so that only the sender and receiver can understand the data. 
* Once the webserver receives the request, it processes it  and sends back an HTTP response.
* If the response was successful, the webserver will direct the browser to a new web page. If an error has occured, one can handle it in multiple ways.

# Submit

* You have recently learned about how forms are sent to web servers and the difference between `GET` and `POST`. In this section, you will build on this konwledge by learning about submit.

## Action and Method

* Form submissions are an essential part of the world wide web. Nearly every website uses forms, from buying items online to ordering food for delivery. When you click the login button on a website, it sends your username and password to a web server to log  you into your accoun.t
* As you know by now, you add a form to your web page using the <b>`<form></form>`</b> tag.
* But how the form is submitted is determined by two essential attributes: <b>action</b> and <b>method</b>.
* The <b>action</b> attribute specifies to which web address the form must be sent. This address is the location of server-side code that will process the request.
```
<form action="/login">
</form>
```
* It is important to note that <b>action</b> can be a full URL address such as <b>https://meta.com</b>, an absolute path such as <b>/login</b>, or a relative path such as <b>login</b>.
* The abosolute path, which <i>starts with a forward slash</i>, will use the base address of the current website, such as <b>https://meta.com</b> and combine it with the absolute path. For example if <b>/login</b> is the absolute path, the form will be submitted to <b>https://meta.com/login</b>. If the address is <b>https://meta.com/company-info/</b> and <b>/login</b> is the absolute path, the submission address will still be <b>https://meta.com/login</b>.
* Similarly, a realtive path will combine the current web address with a relative path. For example, if the web browser is currently on the web page <b>https://meta.com/company-info/</b>, and the relative path is set to <b>login</b>, the form will be submitted to <b>https://meta.com/company-info/login</b>.
* The <b>method</b> attribute specifies which HTTP method is used to submit the form; <b>`GET`</b> or <b>`POST`</b>.
    * Default submission method is <b>`GET`</b>, when <b>method</b> is not specified.
* Forms aren't the only way to submit data to a web server.
* One can also send direct HTTP requests to the web server with the data encapsulated in the request itself in the `JSON` format.

# Additional Resources:

* The following resources will be helpful as additional references in dealing with different concepts related to topics I have covered in the HTML section.
    * [HTML Meta Tags](https://www.dofactory.com/html/metatags).
    * [Semantic elements](https://www.freecodecamp.org/news/semantic-html5-elements/).
    * [Client-side validation of forms with HTML5](https://www.sitepoint.com/client-side-form-validation-html5/).
    * [\<input\> tag in HTML](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input).
    * [Form validation examples](https://www.the-art-of-web.com/html/html5-form-validation/).


# Best Practices

* When writing HTML, it is good practices to semantically describe the content. This allows search engines and accessibility software to understand the contents of a page.
    * This can be done using basic HTML tags. E.g. Using the `<h1>` heading tag describes that the content is a heading.
* It is standard practice for developers to specify their links as an unordered list `<ul>` inside the `<nav>` element.
