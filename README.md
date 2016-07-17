# front-end-developer-test-answer
This is the answer to the test questions


# Technical skills test

This front end development test is intended to cover a broad range of skills required to deliver high quality government digital services. This includes:

* Accessibility
* HTML
* CSS
* jQuery and JavaScript
* Other best practices

Candidates are asked to perform this test remotely and submit their responses to the sender. 

## Accessibility

1. Describe how you would implement the ***'I am looking for...'*** tab panel that appears on [justice.gov.uk](https://www.justice.gov.uk).


# Answer
 This is how I will implement 
 
```html
 <!DOCTYPE html>
<html>
<head>
<style>
ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color: #333;
}

li {
    float: left;
}

li a {
    display: block;
    color: white;
    text-align: center;
    padding: 20px 16px;
    text-decoration: none;
}

li a:hover {
    background-color: #255;
}
</style>
</head>
<body>

<ul>
  <li><a class="active" href="#courts">Courts</a></li>
  <li><a href="#procedure rules">Procedure rule</a></li>
  <li><a href="#offenders">Offenders</a></li>
  <li><a href="#youth justice">Youth justice</a></li>
</ul>

</body>
</html>
```

  Focus specifically on not disadvantaging users of:

  * Assistive technology
  * Older/less featured browsers
  

 # Answer
  *     a) script that displays that the browser is not compatible with Impaired assisted technologies
  *     b) suggest to the user to upgrade the browser.

  Your answer should describe both ***how*** you would do this and describe ***what*** specific features of HTML, ARIA, CSS and JavaScript you would use to achieve this. 
      
      "Assistive technologies are software or equipment that people with disabilities use to improve interaction with the web, 
      such as screen readers that read aloud web pages for people who cannot read text, screen magnifiers for people with some types of low vision, 
      and voice recognition software and selection switches for people who cannot use a keyboard or mouse."
      
        It's easy and relatively inexpensive for website developers to provide transcripts for podcasts and audio files. There are also transcription services that create text transcripts in HTML format.
  
2. How would you implement a version of [GOV.UK browse](https://www.gov.uk/browse/) for a new digital service.

  Your answer should:

  * identify, so far as possible, what GOV.UK have done to ensure accessibility and progressive enhancement
  * assume you're approaching this from scratch
  

 # Answer
    1. Site is mobile friendly, but...
    2. Desktop-size page lack of welcoming screen (I don't know what to do there)
     *   a. Solution : Develop a welcoming message that explains how this section of the site works
     *   b. On mobile : Include a welcome message that explains to tap on the sections to get more information.
 The solution is nothing complex, just a couple paragraphs that describes what the user can do in this page.

```
<p>Welcome</p>
```

## JavaScript and jQuery

1. An exercise using jQuery is provided in test-jquery.html.

2. If you saw this in a Pull Request, what would your advice be:

```javascript
  Array.prototype.split = function(i) { // Adds split to all arrays
      return [this.slice(0, i), this.slice(i)];
  };
```

# Answer
 1. this is just a documentation related to javascript in github
 2. there is not advice for that since it is just documentation! is not a script by itself and it won't be executed.


## CSS

1. What colour would each of the following elements be (Assume each pair of rules are targeting the same element)

# Answer

```css
  h1 {color: red;} -> red
  body h1 {color: green;} -> green

  h2.grape {color: purple;} ->purple (only if <h2 class="grape"> is on the html document
  h2 {color: silver;} -> al the h2 will be silver;

  html > body table tr[id="totals"] td ul > li {color: maroon;} // li has an id of answer -> all li inside of tr#totals will be maroon
  li#answer {color: navy;} -> the li with an id answer will have navy color. <li id="answer"></li>
  
 ```
2. Given the HTML below, write a CSS3 rule that will give prepend the text ‘Tel:’ to the third list item. You are not able to amend the HTML to achieve this.

# Answer

```html
  <style>
    ul li:nth-child(3):before{
    content: "Tel:";
    }
  </style>
  <body>
    <ul>
      <li>JavaScript</li>
      <li>HTML</li>
      <li>Ruby</li>
      <li>Python</li>
    </ul>
  </body>
 ```

3. What changes would you suggest to make these CSS rules ready for a production environment?

# Answer
You usually tend to compress the css code:
    - remove all the spaces
    - remove all the new lines
    - make everything in one line
    
    why?
    bandwidth saving : compressing the css will save bandwidth and improve speed to the page.

```html
  <!DOCTYPE html>
  <html>
      <head>
      <meta charset=utf‐8 />
      <title>Test</title>
        <style type="text/css">
          #one{background‐color: #000;}.three{color:rgba(255,255,255,1);}div>span{border:3px solid green;} 
        </style>
      </head>
      <body>
        <div id="one">
          <div class="three">
            Hello <span>World!</span>
          </div>
        </div>
      </body>
  </html>
```

4. How would you style all links to 'gov.uk' domains differently to other links in an application?

# Answer
1. you "enclose" those links in an id:
```html
<div id="style1">
	<a href="">my link</a>
	<a href="">my link</a>
	<a href="">my link</a>
	<a href="">my link</a>
	<a href="">my link</a>
	<a href="">my link</a>
	<a href="">my link</a>
	<a href="">my link</a>
	<a href="">my link</a>
	<a href="">my link</a>
</div>
```
2. assign a css code to such enclosed section:

```html
<style>
    #style1 a{
        color : rgba(255,50,240,0.5);
        decoration : none;
    }
    #style1 a:hover{
        color : rgba(255,50,240,1);
        decoration : underline;
    }
</style>
```

## HTML

1. A test using HTML5 is provided in test-html.html within this repository.
Please amend the code and submit your changes as a pull request.

## Testing

1. What are **the key things you need to test for** on the front-end of digital services?

 # Answer
    1. compatibility across browsers -> code should work the same in internet explorer, firefox, chrome, opera, etc.
    2. verify that all the content is consisten and check the debugging options of the browser looking for javascript errors or other messages

2. How do you approach testing the front end of applications?

 # Answer
    Every web browser comes with developer options that allows you do certain playgrounds in your current live code in order to help you to fix problems or issues.

## Best practices

1. Is this good quality code? Provide a brief justification of your answer.

```javascript
    <button
      type="button"
      onclick="document.getElementById('xyz').style.color='red';">
        Click Me
    </button>
```
# Answer

     - bad commenting: this is a css comment and content shows html/js code
     - if logic layer is javascript and presentation is HTML, it is bad to mix the logic layer and the presentation layer in one sentence. Each one of them must be separated:
  
 ```javascript
 $("#xyz").click(function(){
    $(this).css("color","red");
 });
``` 

```html
 <button type="button" id="xyz">Click me</button>
``` 
 

2. Describe three ways to decrease page load time (answers may include perceived or actual load times)

# Answer
     a) sources must come from the same domain
     b) javascript files must be condensed in one file as possible to decrease the number of connection to the server
     c) minimizing html css and js code to the point to remove unnecesary spaces, comments 


3. Why is it generally a good idea to position CSS ```<link>```s between ```<head></head>``` and JS ```<script>```s just before ```</body>```? Do you know any exceptions?

# Answer
      a) link MUST be inside of head, since head is the structure where you include css, javascript code and meta data of the page
      b) there is an exception to the rule in the case of javascript. To increase the speed of the pages, HTML5 complains in the w3 indicates that the javascript code must go before the closure of the ```<body>``` tag an example of that if twitter's bootstrap framework where personal js definitions are always defined on the footer
