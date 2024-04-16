### April 14, 2024 - Sunday

Here I am on a nice sunny Sunday, sitting in my warm car with cold wind blowing at Spanish Bank beach's off-leash dog area watching dogs run about. I wanted to write down all that I know about HTML and look up learn more about what I don't.

### Here we go:

```HTML
<!DOCTYPE html>
<html>
  <head>
    <title>my-first-page</title>
  </head>
  <body>
    <img src="./resources/kx-ac-logo.png">
    <h1>Header</h1>
    <p>Text within a paragraph element.</p>
  </body>
</html>
```

The above code snippet is the basic syntax of an HTML document. HTML provides the skeleton of our web pages using tags like `<p>...</p>` which come in pairs (opening & closing though not all of them) to define and organize content. There are `attributes` which provide additional information about the HTML element. 

### Styling:

Once we have the skeleton, we would like to start styling our HTML document. Here's a code snipped with styling elements added:

```HTML
<!DOCTYPE html>
<html>
  <head>
    <title>my-first-page</title>
    <style>
        h1 {
            font-family: sans-serif;
            size: 10em;
            text-align: center;
        }
        .img-container {
            display: flex;
            justify-content: center;
        }
        img {
            width: 100px;
        }
    </style>
  </head>
  <body>
    <div class="img-container">
        <img src="./resources/kx-ac-logo.png">
    </div>
    <h1>Header</h1>
    <p>Welcome to webpage.</p>
    <h2>Awesome things list:</h2>
    <ol>
        <li>Peeling an orange in 1 go</li>
        <li>Empty gym</li>
    </ol>
  </body>
</html>
```

CSS stands for Cascading Style Sheets and is the language in which the design components for the HTML document are written in.

1. **Selectors** are the means by which CSS targets HTML elements to apply styles. 
 - simple element selectors (e.g., `p` for paragraphs)  
 - more complex selectors like class selectors (`.classname`), ID selectors (`#idname`), and pseudo-classes (e.g., `:hover`). 

2. **Properties** are the actual styles you apply to your selected elements, such as `color`, `font-size`, `margin`, `padding`, `border`, and many others. Each property can have different values, which define the specific style settings for those properties (e.g., `color: red;`).

3. **The Box Model**:
   Every element in HTML can be considered as a box. The Box Model consists of margins, borders, padding, and the content itself. 
   ![Box model](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRrbgSyY-segOeh1fbdZLaAgLUXS8NEiipUWrjAJj4ucg&s)
     - **Content**: The area that displays the text or images within the element.
     - **Padding**: Clears an area around the content. The padding is transparent.
     - **Border**: Goes around the padding and content.
     - **Margin**: Clears an area outside the border. The margin does not have a background color, and it is completely transparent.

3. **Cascading** refers to the way CSS rules are applied to HTML elements, and how conflicts are resolved when multiple rules could apply to the same element. Rules are applied in order from least to most specific, and later rules overwrite earlier ones. Styles defined closer to the element in question (inline styles) will generally take precedence over styles defined in `<head>` or external stylesheets.

### Forms and user input:

Here's a simple HTML form to collect a user's name and email address with a submit button.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Simple HTML Form</title>
</head>
<body>
    <form action="/submit-form" method="POST">
        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required>
        
        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>
        
        <button type="submit">Submit</button>
    </form>
</body>
</html>
```

1. `<form>` is the container for the form elements. It has attributes like `action`, which specifies the URL where the form data should be submitted, and `method`, which defines the HTTP method (GET or POST) to be used when submitting the form.
2. The `action` attribute in this example (`/submit-form`) is the URL where the server will receive the form data upon submission. The `method="POST"` indicates that the form data should be sent as part of the request body, suitable for sensitive information like email addresses.
3. `<label>` elements are used to define labels for the `<input>` elements. Each label is associated with an input field through the `for` attribute, which matches the `id` of the corresponding input, enhancing accessibility.
   - `<input type="text">` is an input field for text data. In this case, it's used for the user's name. The `required` attribute makes sure that the user cannot submit the form without filling out this field.
   - `<input type="email">` is specifically for email addresses, which includes built-in validation to ensure the input matches the format of an email address.

4. `<button type="submit">` represents a button that submits the form. The text inside the button ("Submit") is what will appear on the button in the webpage.

