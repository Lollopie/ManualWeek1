## Prompt 1

Create a Website for my Games Store OmniGames. The Website must include three HTML pages:
index.html, about.html and contact.html.
Requirements
The website must include:

1. A valid basic HTML document structure
1. Navigation between all three pages
1. Headings and paragraphs
1. At least one image
1. At least one list
1. Links
1. An About section/page
1. A Contact page
1. A simple contact form
1. Appropriate semantic HTML elements where possible
HTML only. Do not use CSS(even inline), JavaScript, Bootstrap, Tailwind, or other
frameworks/libraries.

### Response

Done. I created the three HTML pages with semantic HTML, navigation, headings, paragraphs, an image, lists, links, an About page, and a contact form—without CSS, JavaScript, or frameworks.
Download the OmniGames HTML files

## Prompt 2

The contact form uses action="#" which is used to allow JS to handle the form, however, the OmniGames website doesn't use JS leading to no post request being sent.

### Response
You're right. `action="#"` doesn't provide a real form submission endpoint. Since the requirement is **HTML only**, the form should either:

1. Use a real server-side endpoint in `action`, or
2. Use `mailto:` if no server exists.

For a purely HTML-only demo, `mailto:` is appropriate because it can open the user's email client without JavaScript.

Replace the form opening tag with:

```html
<form action="mailto:hello@omnigames.example" method="post" enctype="text/plain">
```

So the corrected section is:

```html
<section>
    <h2>Send Us a Message</h2>

    <form action="mailto:hello@omnigames.example" method="post" enctype="text/plain">
        <p>
            <label for="name">Name:</label><br>
            <input type="text" id="name" name="name" required>
        </p>

        <p>
            <label for="email">Email:</label><br>
            <input type="email" id="email" name="email" required>
        </p>

        <p>
            <label for="subject">Subject:</label><br>
            <input type="text" id="subject" name="subject" required>
        </p>

        <p>
            <label for="message">Message:</label><br>
            <textarea id="message" name="message" rows="8" cols="40" required></textarea>
        </p>

        <p>
            <button type="submit">Send Message</button>
        </p>
    </form>
</section>
```

**Important:** `mailto:` does not send an HTTP POST request to a web server. If your assignment specifically requires an actual **POST request**, HTML alone cannot provide the server-side endpoint—you would need something like a PHP/backend form handler.
