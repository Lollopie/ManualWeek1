# Code Comparison

## Entry 1

### Manual version

```html
<nav>
```

### AI version

```html
<nav aria-label="Main navigation">
```

I prefer the AI version to allow for better accessibility.

## Entry 2

### Manual version

```html
<nav>
    <a href="about.html">About us</a>
    <a href="contact.html">Contact</a> 
</nav>
```

### AI version

```html
<nav aria-label="Main navigation">
    <ul>
        <li><a href="index.html">Home</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="contact.html">Contact</a></li>
    </ul>
</nav>
```

I prefer my version not to list the current page to avoid user confusion.

## Entry 3

### Manual version

```html
<img src="storeImage.webp" alt="Image of the OmniGames store">
```

### AI version

```html
<img src="https://images.unsplash.com/photo-1542751371-adc38448a05e?auto=format&fit=crop&w=1000&q=80"
                 alt="Gaming setup with a monitor, keyboard, and controller"
                 width="1000">
```

I prefer the AI version to add explicit image sizing.

## Entry 4

### Manual version

```html
<input type="text" id="fname" name="fname">
```

### AI version:

```html
<input type="text" id="name" name="name" required>
```

I prefer the AI version to explicitly require each input field.

## Entry 5

### Manual version

```html
<input type="text" id="sname" name="sname"><br>
```

### AI version

```html
<p>
    <label for="name">Name:</label><br>
    <input type="text" id="name" name="name" required>
</p>
```

I prefer the AI version to wrap each input / label combo in paragraphs instead of relying on manual line breaks.

## Entry 6

### Manual version

```html
<form>
```

### AI version

```html
<form action="mailto:hello@omnigames.example" method="post" enctype="text/plain">
```

I prefer neither version since the manual version doesn't include any action tag at all and the AI version tries to send
the form over mail which in my opinion is completely impractical.