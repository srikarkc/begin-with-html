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
        <li>Peeling oragne in 1 go</li>
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
   ![Box model](data:image/png;base64,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)
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

