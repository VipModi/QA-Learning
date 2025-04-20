## ✅ **What is the DOM (Document Object Model)?**

**DOM** is a **tree-like structure** that represents everything on a web page — like HTML elements (buttons, text boxes, images, etc.).

When a browser loads a webpage, it reads the HTML and creates a DOM that JavaScript (and jQuery) can interact with.

### 🧠 Think of DOM like:

- HTML becomes a **live object structure**
- JavaScript/jQuery can **read, change, or delete** these objects

---

### ✅ Example of an HTML Document (and its DOM)

```
<!DOCTYPE html>
<html>
  <head>
    <title>Sample Page</title>
  </head>
  <body>
    <h1 id="title">Hello, Vipul!</h1>
    <button onclick="changeTitle()">Click Me</button>
  </body>
</html>
```

The DOM looks like this:
```
html
 ├── head
 │    └── title
 └── body
      ├── h1 (id="title")
      └── button (onclick="changeTitle()")
```

---

## ✅ What is jQuery?

**jQuery** is a **JavaScript library** that makes it easier to **manipulate the DOM** using simpler syntax.

> ✅ jQuery is commonly used in older web apps, and knowing it helps in automation if the page is dynamic.

---

## ✅ DOM Manipulation using jQuery

### 🔹 1. Change Text Content:

```
$('#title').text('Welcome, Tester!');
```

🔍 This changes:
```
<h1 id="title">Hello, Vipul!</h1>
```

⬇️ To:

```
<h1 id="title">Welcome, Tester!</h1>
```

---

### 🔹 2. Change CSS Style:

```
$('#title').css('color', 'blue');
```

✅ Makes the text blue!

---

### 🔹 3. Add or Remove HTML Elements:

```
$('body').append('<p>New paragraph added</p>');
$('#title').remove();
```

---

### 🔹 4. Handle Button Click:

```
$('button').click(function() {
  $('#title').text('Button Clicked!');
});
```

---

## ✅ Why DOM & jQuery Matter in Automation:

- When automating with Selenium, tools interact with the DOM behind the scenes.
    
- You can **inject or execute JavaScript/jQuery** in your scripts to:
    - Wait for elements to appear
    - Click hidden elements
    - Modify elements if needed for testing
        

### 🔧 Example in Selenium (Python):

```
# Executing jQuery via JavaScript to change a heading
driver.execute_script("$('#title').text('Automated!')")
```

---

### ✅ Summary:

|Term|Purpose|
|---|---|
|**DOM**|Live HTML structure of a webpage|
|**jQuery**|JS library to manipulate DOM|
|`$('#id')`|jQuery selector for element|
|`.text()`|Change or get text content|
|`.css()`|Change style|
|`.click()`|Add click behavior|
