# Saha Clothing

# Home Page (index.html)
home_html = """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Clothing Store</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Welcome to Your Clothing Store</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="shop.html">Shop</a>
            <a href="about.html">About</a>
            <a href="contact.html">Contact</a>
        </nav>
    </header>
    <section class="hero">
        <h2>Discover Your Style</h2>
        <p>Browse our collection of high-quality clothing for all occasions.</p>
    </section>
    <section class="highlight">
        <h2>Popular Products</h2>
        <div class="products">
            <div class="product">
                <img src="https://via.placeholder.com/150" alt="Product 1">
                <h3>Flared pants</h3>
                <p>$40.00</p>
            </div>
            <div class="product">
                <img src="https://via.placeholder.com/150" alt="Product 2">
                <h3>Pullover</h3>
                <p>$45.00</p>
            </div>
        <div class="product">
            <img src="https://via.placeholder.com/150" alt="Product 1">
            <h3>jeans</h3></h3>
            <p>$50.00</p>
        </div>
        <div class="product">
            <img src="https://via.placeholder.com/150" alt="Product 2">
            <h3>Hoodie</h3>
            <p>$45.00</p>
        </div>
    </section>
    <footer>
        <p>&copy; 2024 Clothing Store. All rights reserved.</p>
    </footer>
</body>
</html>
"""

# About Page (about.html)
about_html = """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>About Us - Clothing Store</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>About Us</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="shop.html">Shop</a>
            <a href="about.html">About</a>
            <a href="contact.html">Contact</a>
        </nav>
    </header>
    <section>
        <h2>Our Story</h2>
        <p>We are passionate about providing stylish, high-quality clothing for everyone.</p>
    </section>
    <footer>
        <p>&copy; 2024 Clothing Store. All rights reserved.</p>
    </footer>
</body>
</html>
"""

# Contact Page (contact.html)
contact_html = """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact Us - Clothing Store</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>Contact Us</h1>
        <nav>
            <a href="index.html">Home</a>
            <a href="shop.html">Shop</a>
            <a href="about.html">About</a>
            <a href="contact.html">Contact</a>
        </nav>
    </header>
    <section>
        <form>
            <label for="name">Name:</label><br>
            <input type="text" id="name" name="name" required><br><br>
            <label for="email">Email:</label><br>
            <input type="email" id="email" name="email" required><br><br>
            <label for="message">Message:</label><br>
            <textarea id="message" name="message" rows="4" required></textarea><br><br>
            <button type="submit">Send</button>
        </form>
    </section>
    <footer>
        <p>&copy; 2024 Clothing Store. All rights reserved.</p>
    </footer>
</body>
</html>
"""

# CSS File (style.css)
css_content = """
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}
header {
    background-color: #333;
    color: white;
    padding: 1rem;
    text-align: center;
}
nav {
    display: flex;
    justify-content: center;
    background-color: #444;
}
nav a {
    color: white;
    text-decoration: none;
    padding: 1rem;
}
nav a:hover {
    background-color: #555;
}
.hero, .highlight {
    padding: 2rem;
    text-align: center;
    background-color: #f4f4f4;
}
.products {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1rem;
    padding: 1rem;
}
.product {
    border: 1px solid #ddd;
    border-radius: 5px;
    text-align: center;
    padding: 1rem;
}
footer {
    text-align: center;
    padding: 1rem;
    background-color: #333;
    color: white;
}
"""

# Save the files in a zip folder
import zipfile

zip_path = "/mnt/data/ClothingStoreWebsite.zip"
with zipfile.ZipFile(zip_path, 'w') as zip_file:
    zip_file.writestr("index.html", home_html)
    zip_file.writestr("shop.html", shop_html)
    zip_file.writestr("about.html", about_html)
    zip_file.writestr("contact.html", contact_html)
    zip_file.writestr("style.css", css_content)

zip_path

