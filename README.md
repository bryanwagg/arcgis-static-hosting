# README:

Welcome! This repository uses **GitHub Pages** to host simple HTML files, mainly for the purpose of allowing us to embed javascript in an ArcGis Dashboard where it would not normally. Think of this as a way of embedding twice to get it to work. 

It uses **GitHub Actions** to automatically update our “index” (list of files) whenever we add or change HTML documents, along with publishing every file we add as its own webpage.

## How This Repository Works

1. **Every HTML file** you add here will be published on the Github pages website https://bryanwagg.github.io/arcgis-static-hosting/ allowing for easy embedding in ArcGis. 
2. The **index** (the main page) is automatically updated to include a link to any new `.html` files.  
3. You can **add or edit** files directly in GitHub - no special software or coding knowledge needed.

---

## 1. Adding a New HTML File (Using the Template)

We’ve set up a **basic HTML template** that you can copy and edit. Here’s how:

1. In the repository, click on the **Add file** button (usually near the top right).  
2. Select **Create new file** from the dropdown.  
3. In the **Name your file...** box, type the **file name** you want, ending with `.html`.  
   - Example: `windy-wakefield.html`  
4. Paste the **template** below into the large text area and replace the placeholder text.

### Template For Adding Windy Embedded Content (Copy/Paste This)
```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8" />
  <title>Custom Widget</title>
</head>
<body>
<!--
 ADD EMBED CODE HERE
-->
</body>
</html>
```

5. **Edit** the title and content to whatever you like.  
   - **Title**: In the `<title>` tag, name your page e.g. Wakefield Forecast Conditions.

6. When finished, scroll down to the **Commit new file** section.  
   - In the first box labeled **“Commit message,”** type a short description, for example “Add windy-wakefield page.”  
   - Click **Commit new file** to save and publish it.

---

## 2. Editing an Existing File

1. On the main repository page, find the file you want to change and click its name.  
2. Click the **pencil icon** (Edit button) in the upper-right of the file’s view.  
3. Make your changes in the text area.  
4. Scroll down to the **Commit changes** section.  
   - Type a short note describing what you changed.  
   - Click **Commit changes**.

---

## 3. Viewing the Website & Index

1. Go to the GitHub Pages URL:  https://bryanwagg.github.io/arcgis-static-hosting/
2. You should see an **index** page that has a list of links to all our `.html` files.  
3. After adding or editing a file, wait about **1–2 minutes** for the GitHub Action to run (orange dot to turn to green tick on the main repo page). Then refresh the page to see the updated list.
![image](https://github.com/user-attachments/assets/e7fd3473-0a03-4e99-9852-a2168ea035de)


---

## 4. Troubleshooting

1. **I don’t see my new file on the index page.**  
- Wait a minute or two. GitHub Actions needs some time to run. Then refresh.  
- Make sure your file name ends with `.html`.
- Ensure that the deployment has completed (green tick):![image](https://github.com/user-attachments/assets/e7fd3473-0a03-4e99-9852-a2168ea035de)

2. **I made changes, but they’re not showing up on my page.**  
- Try refreshing again or clearing your browser cache. Sometimes changes take a short while to appear.

3. **I accidentally deleted something.**  
- Don’t panic — GitHub saves file histories.  
- We can revert to an older version if needed. Just let me know or we can look at the commit history.

---

## 5. Basic HTML Tips (Optional)

Below are some common HTML elements you can use. **Not all are required** for every page—use only what you need. We’ll also explain the difference between the `<head>` and `<body>` sections in an HTML file.

---

### The Structure of an HTML Document

A very simple HTML page often looks like this:
```html
<!DOCTYPE html>
<html>
    <head>
      <meta charset="UTF-8">
      <title>Page Title</title>
      <!-- The <head> section contains general information about your page:
           - Metadata (like charset)
           - The <title> tag (what appears in the browser tab name)
           - Links to external resources (CSS, scripts)
           - Optional <script> tags -->
    </head>
    <body>
      <!-- The <body> section is what you actually see on the web page:
           - Headings
           - Paragraphs
           - Images
           - Links
           - Inline <script> tags for embedded content
           - Any other content that displays in the browser window -->
    </body>
</html>
```
**Summary**:  
- **`<head>`** is for page metadata and “behind-the-scenes” info (like `<title>` and `<meta>` tags, links to stylesheets, etc.).  
- **`<body>`** is for the content that appears visually in the browser (text, images, headings, etc.).

---
### 1. Embedding Script Tags

- You can include JavaScript for extra functionality using `<script>` tags.

**Where to put `<script>`?**  
- **In the `<head>`** if the script affects the initial rendering of your page.  
- **At the bottom of the `<body>`** so the main content loads first, then the script runs.

Example (placed in the **body**, right before `</body>` for best performance):

    <script>
      alert("Hello! This is a basic script.");
    </script>

> Make sure your script source is from a trusted, secure (HTTPS) location if you use an external script file.

---

## Other HTML types that may not be neccessary here: 
### 1. Headings

- `<h1>` is the largest heading, `<h2>` is smaller, etc.  
- Example (in the **body**):
  
      <h1>Main Title</h1>
      <h2>Subheading</h2>

---

### 2. Paragraphs

- `<p>` is for regular text.  
- Example (in the **body**):
  
      <p>This is a paragraph of text.</p>

---

### 3. Images

- `<img src="IMAGE_URL" alt="DESCRIPTION">`  
- Example (in the **body**):
  
      <img src="https://example.com/image.jpg" alt="Sample Image">
  
- The `alt` attribute helps describe the image—important for accessibility.

---

### 4. Links

- `<a href="URL">Clickable Text</a>`  
- Example (in the **body**):
  
      <a href="https://example.com">Visit Example.com</a>

---

---

### 5. Embedding Other Content

- You can embed external content (like videos or whole web pages) using `<iframe>`:

      <iframe src="https://example.com" width="600" height="400"></iframe>

- `<iframe>` goes in the **body** if you want it displayed on the page.

---

### Remember Not All Tags Are Needed!

- Many HTML tags exist, but you don’t need them all.  
- Add scripts and other embedded content you want to appear in ArcGis Dashboards, and then add iframes, links, images or other elements only when you actually need them.

---

**Remember**: Keep it simple! Over time, you can experiment with more complex HTML features, but focusing on `<body>` content (and those pesky embedded `<script>` tags is often all you will need.

You don’t need to know everything at once. Simple text edits are fine. Over time, you can explore adding more interesting content to your pages.

---
