# Fork
Fork est une marque de vêtements qui célèbre l'individualité avec des designs uniques et de haute qualité. Inspirée par l'énergie urbaine, Fork propose des pièces modernes et audacieuses pour ceux qui veulent affirmer leur style. Chaque collection est pensée pour s’adapter à toutes les personnalités avec authenticité et originalité.



  
</head>
<body>
    <header>
        <h1>Fork</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="shop.html">Shop</a>
            <a href="about.html">About</a>
            <a href="contact.html">Contact</a>
        </nav>
    </header>
    <section class="hero">
        <h2>Welcome to Fork</h2>
        <p>Your go-to brand for unique style and quality.</p>
    </section>
</body>
</html>
""",
    'shop.html': """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fork - Shop</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Fork</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="shop.html">Shop</a>
            <a href="about.html">About</a>
            <a href="contact.html">Contact</a>
        </nav>
    </header>
    <section class="products">
        <h2>Our Collection</h2>
        <div class="product-list">
            <div class="product-item">Product 1</div>
            <div class="product-item">Product 2</div>
            <div class="product-item">Product 3</div>
            <!-- Add more products as needed -->
        </div>
    </section>
</body>
</html>
""",
    'about.html': """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fork - About</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Fork</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="shop.html">Shop</a>
            <a href="about.html">About</a>
            <a href="contact.html">Contact</a>
        </nav>
    </header>
    <section class="about">
        <h2>About Fork</h2>
        <p>Fork is a brand that values creativity, style, and quality. We believe in making fashion accessible and unique.</p>
    </section>
</body>
</html>
""",
    'contact.html': """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fork - Contact</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Fork</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="shop.html">Shop</a>
            <a href="about.html">About</a>
            <a href="contact.html">Contact</a>
        </nav>
    </header>
    <section class="contact">
        <h2>Contact Us</h2>
        <form>
            <label for="name">Name:</label>
            <input type="text" id="name" name="name" required>
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required>
            <label for="message">Message:</label>
            <textarea id="message" name="message" required></textarea>
            <button type="submit">Send</button>
        </form>
    </section>
</body>
</html>
""",
    'styles.css': """
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

body {
    line-height: 1.6;
    background-color: #f5f5f5;
    color: #333;
}

header {
    background-color: #333;
    color: #fff;
    padding: 1rem;
    text-align: center;
}

header nav a {
    color: #fff;
    margin: 0 15px;
    text-decoration: none;
}

.hero {
    padding: 2rem;
    text-align: center;
    background-color: #e3f2fd;
}

.products, .about, .contact {
    padding: 2rem;
    text-align: center;
}

.product-list {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    margin-top: 1rem;
}

.product-item {
    background: #ccc;
    width: 30%;
    padding: 1rem;
    margin: 0.5rem;
    border-radius: 5px;
    text-align: center;
}

form {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
}

input, textarea, button {
    padding: 0.5rem;
    width: 80%;
    max-width: 400px;
}

button {
    background-color: #333;
    color: #fff;
    border: none;
    cursor: pointer;
}

button:hover {
    background-color: #555;
}
"""
}

# Creating a zip file to store these files
zip_path = "/mnt/data/Fork_website.zip"
with ZipFile(zip_path, 'w') as zipf:
    for filename, content in site_structure.items():
        # Write each file with its respective content
        zipf.writestr(filename, content)

zip_path
