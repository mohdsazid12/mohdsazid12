your-ecommerce-website/
├── index.html
├── product.html
├── styles.css
├── scripts.js
└── images/
    └── product1.jpg
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Your E-commerce Website</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Welcome to Your E-commerce Store</h1>
    </header>
    <main>
        <h2>Featured Products</h2>
        <div class="product-list">
            <div class="product">
                <img src="images/product1.jpg" alt="Product 1">
                <h3>Product 1</h3>
                <p>$19.99</p>
                <a href="product.html">View Product</a>
            </div>
        </div>
    </main>
    <footer>
        <p>&copy; 2024 Your E-commerce Store</p>
    </footer>
    <script src="scripts.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Product 1 - Your E-commerce Store</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Product 1</h1>
    </header>
    <main>
        <div class="product-detail">
            <img src="images/product1.jpg" alt="Product 1">
            <div class="product-info">
                <h2>Product 1</h2>
                <p>$19.99</p>
                <p>This is a great product.</p>
                <button onclick="addToCart()">Add to Cart</button>
            </div>
        </div>
    </main>
    <footer>
        <p>&copy; 2024 Your E-commerce Store</p>
    </footer>
    <script src="scripts.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1rem 0;
}

main {
    padding: 2rem;
}

.product-list {
    display: flex;
    justify-content: space-around;
}

.product {
    background-color: white;
    padding: 1rem;
    text-align: center;
    border: 1px solid #ddd;
    border-radius: 4px;
}

.product img {
    width: 100%;
    max-width: 200px;
    height: auto;
}

.product h3 {
    margin: 1rem 0 0.5rem;
}

.product p {
    margin: 0.5rem 0;
}

.product-detail {
    display: flex;
    justify-content: space-around;
    padding: 2rem 0;
}

.product-detail img {
    width: 50%;
    height: auto;
}

.product-info {
    padding: 1rem;
    max-width: 400px;
}

footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 1rem 0;
    position: fixed;
    bottom: 0;
    width: 100%;
}
function addToCart() {
    alert('Product added to cart!');
    // Add functionality to actually add the product to the cart
}
const express = require('express');
const app = express();
const port = 3000;

app.use(express.static('public'));

app.get('/', (req, res) => {
    res.sendFile(__dirname + '/index.html');
});

app.listen(port, () => {
    console.log(`Server running at http://localhost:${port}`);
});
npm init -y
npm install express
node server.js
