# URL Decoder Documentation

## Overview
This is a simple web-based tool that decodes URL-encoded text. If a URL contains encoded characters like `%20` (for spaces), `%3A` (for `:`), or `%2F` (for `/`), this tool converts them back to their original readable format.

## How to Use
1. Open the HTML file in a web browser.
2. Paste an encoded URL into the input box.
3. Click the **"Decode"** button.
4. The decoded URL will be displayed below the button.

## Code Explanation

### 1. HTML Structure
- `<h2>`: Displays the title "URL Decoder".
- `<input>`: A text box where users can enter the encoded URL.
- `<button>`: When clicked, it calls the `decodeUrl()` function.
- `<p><span>`: Displays the decoded URL.

### 2. CSS Styling
- The body text is centered and uses the Arial font.
- The input box takes up 80% of the width, with padding for better appearance.
- The button is styled with a blue background and changes color on hover.

### 3. JavaScript Function
```javascript
function decodeUrl() {
    let input = document.getElementById("encodedUrl").value;
    document.getElementById("decodedOutput").innerText = decodeURIComponent(input);
}
```
- `document.getElementById("encodedUrl").value`: Gets the user-inputted URL.
- `decodeURIComponent(input)`: Decodes the URL by converting encoded characters back to normal.
- `document.getElementById("decodedOutput").innerText = ...`: Displays the decoded URL in the webpage.

## Example
### Input:
```
https%3A%2F%2Fexample.com%2Fhello%20world
```
### Output:
```
https://example.com/hello world
```
