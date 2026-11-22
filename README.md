# Lab 4b: JavaScript, JSON & jQuery

-**Name:** SITI NURSHAFIQA FIRDAUS  
-**Matric No.:** AI250145  
## Project Structure
- `Q1/` — Question 1 files
- `Q2/` — `books.html`
- `Q3/` — `jquery-dom.html`
- `Output screenshots/`  
- Output Q1:
  ![Q1 Output](ss/Q1.png)
- Output Q2:
  ![Q2 Output](ss/Q2.png)
- Output Q3:
  ![Q3 Before](ss/Q3.1.png)  
  ![Q3 After](ss/Q3.2.png)

## Question 2: Fetching & Displaying Book Data (`books.html` & `books.json`)
- **How it works:** Uses `fetch()` and `await` inside `loadBooks()` to read `books.json`, parse the JSON data, and dynamically update the DOM for the first book's title, the second book's author, and the list of genres grouped by book title.
- **Issues I resolved:**
  1. **CORS / Local Server:** Opening `books.html` directly via `file://` triggered a CORS error when fetching `books.json`, so the page was run through **VS Code Live Server**.
  2. **Fetch Path (`404 Not Found`):** Updated the `fetch()` path to match where `books.json` is located relative to `Q2/books.html`.
  3. **Missing DOM Element (`TypeError`):** Added the `#secondAuthor` element in `books.html` and guarded DOM updates in the `catch` block so `textContent` is not set on `null`.

## Question 3: jQuery DOM Manipulation & Events (`jquery-dom.html`)
- **How it works:** Waits for the document to be ready with `$(function () { ... })` and performs three jQuery operations:
  1. Replaces `#myElement` text with `"Modified Text"` using `.text("Modified Text")`.
  2. Adds the `myStyle` class to `#myDIV` using `.addClass("myStyle")`.
  3. Listens for a click on `#myButton` using `.on("click", ...)` and displays an alert saying `"Button clicked!"`.

## Output Screenshots

### Q2 Output (via Live Server)
![Q2 Output](ss/Q2.png)

### Q3 Output (Before / After Click)
![Q3 Before Click](ss/Q3.1.png)  
![Q3 Ater Clicked](ss/Q3.2.png)