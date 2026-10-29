<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ShopEase - Online Shopping</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body {
            background-color: #f5f5f5;
            color: #333;
        }

        header {
            background-color: #2874f0;
            color: white;
            padding: 20px 7%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 15px;
        }

        header h1 {
            font-size: 28px;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 0 10px;
            font-weight: bold;
        }

        .search {
            padding: 10px;
            border: none;
            border-radius: 5px;
            width: 220px;
            max-width: 100%;
        }

        .banner {
            background: linear-gradient(120deg, #ff9a44, #fc6076);
            color: white;
            text-align: center;
            padding: 55px 20px;
        }

        .banner h2 {
            font-size: 36px;
            margin-bottom: 12px;
        }

        .banner p {
            font-size: 18px;
            margin-bottom: 20px;
        }

        .banner a {
            display: inline-block;
            background: white;
            color: #e64a19;
            padding: 12px 25px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: bold;
        }

        .categories {
            text-align: center;
            padding: 30px 15px;
            background: white;
        }

        .categories h2,
        .products-section h2 {
            margin-bottom: 20px;
            color: #222;
        }

        .category-list {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 15px;
        }

        .category {
            background: #e8f0fe;
            color: #174ea6;
            padding: 12px 22px;
            border-radius: 25px;
            font-weight: bold;
        }

        .products-section {
            padding: 35px 7%;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(4, minmax(0, 1fr));
            gap: 22px;
        }

        .product-card {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 3px 12px #00000012;
            transition: transform 0.3s;
        }

        .product-card:hover {
            transform: translateY(-5px);
        }

        .product-image {
            height: 190px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: #f0f3f8;
            font-size: 85px;
        }

        .product-info {
            padding: 18px;
        }

        .product-info h3 {
            margin-bottom: 10px;
            font-size: 18px;
        }

        .description {
            color: #666;
            font-size: 14px;
            line-height: 1.5;
            min-height: 42px;
        }

        .rating {
            color: #16803c;
            margin: 12px 0;
            font-weight: bold;
        }

        .price {
            font-size: 21px;
            font-weight: bold;
            margin-bottom: 8px;
        }

        .old-price {
            font-size: 14px;
            color: #888;
            text-decoration: line-through;
            margin-left: 5px;
        }

        .discount {
            color: #16803c;
            font-size: 14px;
            font-weight: bold;
            margin-bottom: 15px;
        }

        .buy-button {
            display: block;
            width: 100%;
            padding: 12px;
            background: #2874f0;
            color: white;
            text-align: center;
            text-decoration: none;
            border: none;
            border-radius: 5px;
            font-size: 15px;
            cursor: pointer;
        }

        .buy-button:hover {
            background: #1558bd;
        }

        .offer-banner {
            margin: 10px 7% 35px;
            padding: 30px 20px;
            background: #172337;
            color: white;
            text-align: center;
            border-radius: 10px;
        }

        .offer-banner h2 {
            margin-bottom: 10px;
        }

        footer {
            background: #172337;
            color: white;
            text-align: center;
            padding: 25px 15px;
            line-height: 1.8;
        }

        @media (max-width: 1000px) {
            .product-grid {
                grid-template-columns: repeat(2, minmax(0, 1fr));
            }
        }

        @media (max-width: 600px) {
            header {
                flex-direction: column;
                text-align: center;
            }

            nav a {
                display: inline-block;
                margin: 5px;
            }

            .search {
                width: 100%;
            }

            .banner h2 {
                font-size: 27px;
            }

            .product-grid {
                grid-template-columns: 1fr;
            }

            .product-image {
                height: 170px;
            }

            .products-section {
                padding: 25px 5%;
            }
        }
    </style>
</head>

<body>

    <header>
        <h1>ShopEase</h1>

        <input
            type="search"
            class="search"
            placeholder="Search products..."
            aria-label="Search products"
        >

        <nav>
            <a href="#home">Home</a>
            <a href="#categories">Categories</a>
            <a href="#products">Products</a>
            <a href="#contact">Contact</a>
        </nav>
    </header>

    <section class="banner" id="home">
        <h2>Big Shopping Festival!</h2>
        <p>Discover amazing deals with discounts up to 50%.</p>
        <a href="#products">Shop Now</a>
    </section>

    <section class="categories" id="categories">
        <h2>Shop by Category</h2>

        <div class="category-list">
            <div class="category">Electronics</div>
            <div class="category">Fashion</div>
            <div class="category">Footwear</div>
            <div class="category">Accessories</div>
        </div>
    </section>

    <section class="products-section" id="products">
        <h2>Featured Products</h2>

        <div class="product-grid">

            <article class="product-card">
                <div class="product-image">🎧</div>
                <div class="product-info">
                    <h3>Wireless Headphones</h3>
                    <p class="description">
                        Enjoy clear sound, comfortable ear cushions
                        and wireless connectivity.
                    </p>
                    <p class="rating">★ 4.5 | 125 reviews</p>
                    <p class="price">
                        ₹1,499
                        <span class="old-price">₹2,999</span>
                    </p>
                    <p class="discount">50% OFF</p>
                    <button class="buy-button" type="button"
                        onclick="alert('Wireless Headphones selected!')">
                        Buy Now
                    </button>
                </div>
            </article>

            <article class="product-card">
                <div class="product-image">⌚</div>
                <div class="product-info">
                    <h3>Smart Watch</h3>
                    <p class="description">
                        Track daily activity and view notifications
                        with a stylish digital display.
                    </p>
                    <p class="rating">★ 4.3 | 98 reviews</p>
                    <p class="price">
                        ₹1,999
                        <span class="old-price">₹3,499</span>
                    </p>
                    <p class="discount">43% OFF</p>
                    <button class="buy-button" type="button"
                        onclick="alert('Smart Watch selected!')">
                        Buy Now
                    </button>
                </div>
            </article>

            <article class="product-card">
                <div class="product-image">👟</div>
                <div class="product-info">
                    <h3>Running Shoes</h3>
                    <p class="description">
                        Lightweight shoes designed for everyday
                        comfort and running.
                    </p>
                    <p class="rating">★ 4.2 | 76 reviews</p>
                    <p class="price">
                        ₹1,299
                        <span class="old-price">₹2,499</span>
                    </p>
                    <p class="discount">48% OFF</p>
                    <button class="buy-button" type="button"
                        onclick="alert('Running Shoes selected!')">
                        Buy Now
                    </button>
                </div>
            </article>

            <article class="product-card">
                <div class="product-image">🎒</div>
                <div class="product-info">
                    <h3>Travel Backpack</h3>
                    <p class="description">
                        A spacious backpack with multiple pockets
                        for college and travel.
                    </p>
                    <p class="rating">★ 4.6 | 150 reviews</p>
                    <p class="price">
                        ₹899
                        <span class="old-price">₹1,499</span>
                    </p>
                    <p class="discount">40% OFF</p>
                    <button class="buy-button" type="button"
                        onclick="alert('Travel Backpack selected!')">
                        Buy Now
                    </button>
                </div>
            </article>

        </div>
    </section>

    <section class="offer-banner">
        <h2>Special Weekend Offer</h2>
        <p>Extra savings on your favourite products. Shop today!</p>
    </section>

    <footer id="contact">
        <h3>ShopEase Online Store</h3>
        <p>Email: support@shopease.example</p>
        <p>Customer Support: Monday - Saturday</p>
        <p>&copy; 2026 ShopEase. All rights reserved.</p>
    </footer>

</body>
</html>
