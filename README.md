# rabi-acne-care
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ACNE CARE Store</title>

<style>
    body {
        font-family: Arial, sans-serif;
        background: #f7f7f7;
        padding: 20px;
    }

    h1 {
        text-align: center;
        color: #333;
    }

    .product-container {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 20px;
    }

    .product {
        background: white;
        padding: 15px;
        border-radius: 10px;
        box-shadow: 0 0 5px rgba(0,0,0,0.1);
        text-align: center;
    }

    .product button {
        margin-top: 10px;
        padding: 10px 15px;
        background: #0099ff;
        color: white;
        border: none;
        border-radius: 5px;
    }

    #cart {
        margin-top: 30px;
        background: white;
        padding: 15px;
        border-radius: 10px;
    }
</style>
</head>

<body>

<h1>ACNE CARE - Online Store</h1>

<div class="product-container">

    <div class="product">
        <h3>Dorskin Acne</h3>
        <p>Price: Rp 100.000.000</p>
        <button onclick="addToCart('Dorskin Acne', 100000000)">Add to Cart</button>
    </div>

    <div class="product">
        <h3>Dorskin Brightening</h3>
        <p>Price: Rp 110.000.000</p>
        <button onclick="addToCart('Dorskin Brightening', 110000000)">Add to Cart</button>
    </div>

    <div class="product">
        <h3>Serum Acne</h3>
        <p>Price: Rp 140.000.000</p>
        <button onclick="addToCart('Serum Acne', 140000000)">Add to Cart</button>
    </div>

    <div class="product">
        <h3>Serum Brightening</h3>
        <p>Price: Rp 145.000.000</p>
        <button onclick="addToCart('Serum Brightening', 145000000)">Add to Cart</button>
    </div>

    <div class="product">
        <h3>Toner Calm Acne</h3>
        <p>Price: Rp 75.000.000</p>
        <button onclick="addToCart('Toner Calm Acne', 75000000)">Add to Cart</button>
    </div>

    <div class="product">
        <h3>Toner Whitening</h3>
        <p>Price: Rp 150.000.000</p>
        <button onclick="addToCart('Toner Whitening', 150000000)">Add to Cart</button>
    </div>

    <div class="product">
        <h3>Face Wash Acne Care</h3>
        <p>Price: Rp 700.000.000</p>
        <button onclick="addToCart('Face Wash Acne Care', 700000000)">Add to Cart</button>
    </div>

</div>

<!-- CART -->
<div id="cart">
    <h2>Your Cart</h2>
    <ul id="cartItems"></ul>
    <h3 id="totalPrice">Total: Rp 0</h3>
</div>

<script>
    let cart = [];
    let total = 0;

    function addToCart(name, price) {
        cart.push({name, price});
        total += price;
        updateCart();
    }

    function updateCart() {
        let list = "";
        cart.forEach(item => {
            list += `<li>${item.name} - Rp ${item.price.toLocaleString()}</li>`;
        });
        document.getElementById("cartItems").innerHTML = list;
        document.getElementById("totalPrice").innerHTML = "Total: Rp " + total.toLocaleString();
    }
</script>

</body>
</html>
