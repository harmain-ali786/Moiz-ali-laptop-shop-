# only for the sample not an real website make by harmain-
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>moiz ali laptop shop</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }

        body {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 20px;
        }

        .container {
            width: 100%;
            max-width: 400px;
            margin: 0 auto;
        }

        .logo-container {
            text-align: center;
            margin-bottom: 30px;
            perspective: 1000px;
        }

        .logo {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            object-fit: cover;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            transform-style: preserve-3d;
            transition: transform 0.5s ease;
        }

        .logo:hover {
            transform: rotateY(15deg) scale(1.05);
        }

        .shop-name {
            font-size: 28px;
            font-weight: 700;
            color: #2c3e50;
            margin-top: 15px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }

        .product-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
            transform-style: preserve-3d;
            transition: transform 0.5s ease, box-shadow 0.5s ease;
            margin-bottom: 30px;
        }

        .product-card:hover {
            transform: translateY(-10px) rotateX(5deg);
            box-shadow: 0 25px 50px rgba(0, 0, 0, 0.15);
        }

        .product-images {
            position: relative;
            height: 250px;
            overflow: hidden;
        }

        .image-slider {
            display: flex;
            transition: transform 0.5s ease;
            height: 100%;
        }

        .product-image {
            min-width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .slider-nav {
            position: absolute;
            bottom: 15px;
            left: 0;
            right: 0;
            display: flex;
            justify-content: center;
            gap: 8px;
        }

        .slider-dot {
            width: 10px;
            height: 10px;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.5);
            cursor: pointer;
            transition: background 0.3s ease, transform 0.3s ease;
        }

        .slider-dot.active {
            background: white;
            transform: scale(1.2);
        }

        .product-info {
            padding: 25px;
        }

        .product-title {
            font-size: 18px;
            font-weight: 600;
            color: #2c3e50;
            margin-bottom: 15px;
            line-height: 1.4;
        }

        .product-price {
            font-size: 24px;
            font-weight: 700;
            color: #e74c3c;
            margin-bottom: 20px;
        }

        .view-product-btn {
            display: block;
            width: 100%;
            padding: 15px;
            background: linear-gradient(135deg, #3498db 0%, #2980b9 100%);
            color: white;
            border: none;
            border-radius: 12px;
            font-size: 16px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 5px 15px rgba(52, 152, 219, 0.4);
            transform-style: preserve-3d;
            position: relative;
            overflow: hidden;
        }

        .view-product-btn:hover {
            background: linear-gradient(135deg, #2980b9 0%, #3498db 100%);
            transform: translateY(-3px) scale(1.02);
            box-shadow: 0 8px 20px rgba(52, 152, 219, 0.6);
        }

        .view-product-btn:active {
            transform: translateY(1px) scale(0.98);
        }

        .view-product-btn::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(255, 255, 255, 0.2);
            transform: translateX(-100%) rotate(45deg);
            transition: transform 0.5s ease;
        }

        .view-product-btn:hover::after {
            transform: translateX(100%) rotate(45deg);
        }

        .features {
            margin-top: 30px;
            background: white;
            border-radius: 20px;
            padding: 25px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.08);
            transform-style: preserve-3d;
            transition: transform 0.3s ease;
        }

        .features:hover {
            transform: translateY(-5px);
        }

        .features-title {
            font-size: 20px;
            font-weight: 600;
            color: #2c3e50;
            margin-bottom: 15px;
            text-align: center;
        }

        .feature-list {
            list-style: none;
        }

        .feature-item {
            padding: 10px 0;
            border-bottom: 1px solid #f1f1f1;
            display: flex;
            align-items: center;
        }

        .feature-item:last-child {
            border-bottom: none;
        }

        .feature-icon {
            width: 24px;
            height: 24px;
            margin-right: 10px;
            color: #3498db;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .fade-in {
            animation: fadeIn 0.8s ease forwards;
        }

        @media (max-width: 480px) {
            .container {
                padding: 0 10px;
            }
            
            .product-title {
                font-size: 16px;
            }
            
            .product-price {
                font-size: 22px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="logo-container fade-in">
            <img src="https://i.postimg.cc/139rDF9R/IMG-20250929-144502.jpg" alt="moiz ali laptop shop logo" class="logo">
            <h1 class="shop-name">moiz ali laptop shop</h1>
        </div>

        <div class="product-card fade-in">
            <div class="product-images">
                <div class="image-slider" id="imageSlider">
                    <img src="https://i.postimg.cc/h4LmMGZh/IMG-20250929-142147.jpg" alt="Dell XPS 9500 Laptop" class="product-image">
                    <img src="https://i.postimg.cc/2j0kzRVv/IMG-20250929-142208.jpg" alt="Dell XPS 9500 Laptop" class="product-image">
                    <img src="https://i.postimg.cc/ZYXT9Pxr/IMG-20250929-142226.jpg" alt="Dell XPS 9500 Laptop" class="product-image">
                    <img src="https://i.postimg.cc/k42SfXbB/IMG-20250929-142249.jpg" alt="Dell XPS 9500 Laptop" class="product-image">
                </div>
                <div class="slider-nav">
                    <div class="slider-dot active" data-index="0"></div>
                    <div class="slider-dot" data-index="1"></div>
                    <div class="slider-dot" data-index="2"></div>
                    <div class="slider-dot" data-index="3"></div>
                </div>
            </div>
            <div class="product-info">
                <h2 class="product-title">Dell XPS 9500 Core i7 10th Gen | 4GB GTX 1650Ti | 16GB RAM | 512GB SSD</h2>
                <div class="product-price">Rs. 1.6 Lacs</div>
                <button class="view-product-btn" id="viewProductBtn">View Product</button>
            </div>
        </div>

        <div class="features fade-in">
            <h3 class="features-title">Key Features</h3>
            <ul class="feature-list">
                <li class="feature-item">
                    <svg class="feature-icon" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                    </svg>
                    10th Generation Intel Core i7 Processor
                </li>
                <li class="feature-item">
                    <svg class="feature-icon" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                    </svg>
                    4GB NVIDIA GeForce GTX 1650Ti Graphics
                </li>
                <li class="feature-item">
                    <svg class="feature-icon" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                    </svg>
                    16GB RAM for Smooth Multitasking
                </li>
                <li class="feature-item">
                    <svg class="feature-icon" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
                        <path fill-rule="evenodd" d="M16.707 5.293a1 1 0 010 1.414l-8 8a1 1 0 01-1.414 0l-4-4a1 1 0 011.414-1.414L8 12.586l7.293-7.293a1 1 0 011.414 0z" clip-rule="evenodd"></path>
                    </svg>
                    512GB SSD for Fast Storage
                </li>
            </ul>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Image slider functionality
            const slider = document.getElementById('imageSlider');
            const dots = document.querySelectorAll('.slider-dot');
            let currentSlide = 0;
            const slideCount = 4;
            
            // Set initial slider position
            slider.style.transform = `translateX(0)`;
            
            // Add click events to dots
            dots.forEach(dot => {
                dot.addEventListener('click', function() {
                    const index = parseInt(this.getAttribute('data-index'));
                    goToSlide(index);
                });
            });
            
            function goToSlide(index) {
                currentSlide = index;
                slider.style.transform = `translateX(-${currentSlide * 100}%)`;
                
                // Update active dot
                dots.forEach((dot, i) => {
                    if (i === currentSlide) {
                        dot.classList.add('active');
                    } else {
                        dot.classList.remove('active');
                    }
                });
            }
            
            // Auto slide every 5 seconds
            setInterval(() => {
                currentSlide = (currentSlide + 1) % slideCount;
                goToSlide(currentSlide);
            }, 5000);
            
            // Button click event
            document.getElementById('viewProductBtn').addEventListener('click', function() {
                window.location.href = 'https://www.olx.com.pk/item/dell-xps-9500-core-i7-10th-gen-4gb-card-gtx-1650ti-16512gb-model-iid-1105112911';
            });
            
            // Add fade-in animation to elements
            const fadeElements = document.querySelectorAll('.fade-in');
            fadeElements.forEach((element, index) => {
                element.style.animationDelay = `${index * 0.2}s`;
            });
        });
    </script>
