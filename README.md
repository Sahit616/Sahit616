# Writing an HTML and CSS template for a basic clothing sales website

html_content = """
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Clothing Store</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            box-sizing: border-box;
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
        .hero {
            text-align: center;
            padding: 2rem;
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
        .product img {
            max-width: 100%;
            border-radius: 5px;
        }
        footer {
            text-align: center;
            padding: 1rem;
            background-color: #333;
            color: white;
        }
    </style>
</head>
<body>

<header>
    <h1>Welcome to Your Clothing Store</h1>
</header>

<nav>
    <a href="#home">Home</a>
    <a href="#products">Products</a>
    <a href="#about">About Us</a>
    <a href="#contact">Contact</a>
</nav>

<div class="hero" id="home">
    <h2>Discover Your Style</h2>
    <p>Browse our collection of high-quality clothing for all occasions.</p>
</div>

<section class="products" id="products">
    <div class="product">
        <img src="https://via.placeholder.com/150" alt="Product 1">
        <h3>Product 1</h3>
        <p>$20.00</p>
    </div>
    <div class="product">
        <img src="https://via.placeholder.com/150" alt="Product 2">
        <h3>Product 2</h3>
        <p>$25.00</p>
    </div>
    <div class="product">
        <img src="https://via.placeholder.com/150" alt="Product 3">
        <h3>Product 3</h3>
        <p>$30.00</p>
    </div>
</section>

<section id="about">
    <h2>About Us</h2>
    <p>We are passionate about providing stylish, high-quality clothing for everyone.</p>
</section>

<section id="contact">
    <h2>Contact Us</h2>
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
    <p>&copy; 2024 Your Clothing Store. All rights reserved.</p>
</footer>

</body>
</html>
"""

# Save the HTML content to a file
file_path = "/mnt/data/ClothingStore.html"
with open(file_path, "w") as file:
    file.write(html_content)

file_path
