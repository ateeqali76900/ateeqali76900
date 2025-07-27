<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Apple Orchard Paradise | Family Farm</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Roboto:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #8BC34A;
            --secondary: #FF5722;
            --accent: #4CAF50;
            --dark: #4E342E;
            --light: #FFF9C4;
            --text: #333333;
            --white: #ffffff;
        }

        body {
            font-family: 'Roboto', sans-serif;
            color: var(--text);
            line-height: 1.6;
            background-color: #f9f6f1;
        }

        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            font-weight: 700;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }

        /* Header Styles */
        header {
            background-color: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            padding: 15px 0;
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
        }

        .logo img {
            height: 50px;
            margin-right: 10px;
        }

        .logo h1 {
            font-size: 1.8rem;
            color: var(--accent);
        }

        .logo span {
            color: var(--secondary);
        }

        nav ul {
            display: flex;
            list-style: none;
        }

        nav ul li {
            margin-left: 25px;
        }

        nav ul li a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            font-size: 1.1rem;
            transition: color 0.3s;
        }

        nav ul li a:hover {
            color: var(--secondary);
        }

        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: white;
            padding: 12px 25px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            font-size: 1rem;
        }

        .btn:hover {
            background-color: #e64a19;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(255, 87, 34, 0.3);
        }

        /* Hero Section */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)), url('https://images.unsplash.com/photo-1471194402529-8e0f5a675de6?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1950&q=80') no-repeat center center/cover;
            display: flex;
            align-items: center;
            text-align: center;
            color: var(--white);
            padding-top: 70px;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h2 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }

        .hero p {
            font-size: 1.5rem;
            margin-bottom: 30px;
            text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.5);
        }

        /* Sections */
        section {
            padding: 80px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title h2 {
            font-size: 2.5rem;
            color: var(--dark);
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }

        .section-title h2:after {
            content: '';
            position: absolute;
            width: 70px;
            height: 3px;
            background-color: var(--secondary);
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
        }

        /* About Section */
        .about-content {
            display: flex;
            align-items: center;
            gap: 40px;
        }

        .about-text {
            flex: 1;
        }

        .about-image {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .about-image img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s;
        }

        .about-image:hover img {
            transform: scale(1.05);
        }

        /* Products Section */
        .products {
            background-color: var(--light);
        }

        .apple-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .apple-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s;
        }

        .apple-card:hover {
            transform: translateY(-10px);
        }

        .apple-image {
            height: 200px;
            overflow: hidden;
        }

        .apple-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }

        .apple-card:hover .apple-image img {
            transform: scale(1.1);
        }

        .apple-info {
            padding: 20px;
            text-align: center;
        }

        .apple-info h3 {
            color: var(--dark);
            margin-bottom: 10px;
        }

        .apple-info p {
            color: #777;
            margin-bottom: 15px;
        }

        /* Visit Section */
        .visit-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .visit-card {
            background-color: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            text-align: center;
        }

        .visit-icon {
            font-size: 3rem;
            color: var(--secondary);
            margin-bottom: 20px;
        }

        /* Contact Section */
        .contact {
            background-color: var(--primary);
            color: white;
        }

        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }

        .contact-info h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
        }

        .contact-details {
            margin-bottom: 30px;
        }

        .contact-details p {
            margin-bottom: 10px;
            display: flex;
            align-items: center;
        }

        .contact-details i {
            margin-right: 10px;
            width: 25px;
        }

        .social-icons {
            display: flex;
            gap: 15px;
        }

        .social-icons a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: white;
            color: var(--primary);
            border-radius: 50%;
            font-size: 1.2rem;
            transition: all 0.3s;
        }

        .social-icons a:hover {
            background-color: var(--secondary);
            color: white;
            transform: translateY(-5px);
        }

        .contact-form {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            color: var(--dark);
            font-weight: 500;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: 'Roboto', sans-serif;
            font-size: 1rem;
        }

        .form-group textarea {
            height: 150px;
            resize: vertical;
        }

        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 40px 0 20px;
            text-align: center;
        }

        .footer-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            margin-bottom: 30px;
        }

        .footer-column {
            flex: 1;
            min-width: 250px;
            margin-bottom: 30px;
        }

        .footer-column h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-column h3:after {
            content: '';
            position: absolute;
            width: 40px;
            height: 2px;
            background-color: var(--secondary);
            bottom: 0;
            left: 0;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 10px;
        }

        .footer-column ul li a {
            color: #ccc;
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-column ul li a:hover {
            color: var(--secondary);
        }

        .copyright {
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            color: #aaa;
        }

        /* Responsive */
        @media (max-width: 992px) {
            .about-content {
                flex-direction: column;
            }
            
            .hero h2 {
                font-size: 2.8rem;
            }
            
            .hero p {
                font-size: 1.2rem;
            }
        }

        @media (max-width: 768px) {
            nav ul {
                display: none;
            }
            
            .hero h2 {
                font-size: 2.3rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">
                <img src="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNTYgMjU2Ij48cGF0aCBmaWxsPSIjNEVCMzQyIiBkPSJNMjI0LDY0YTk2LDk2LDAsMCwwLTE5MiwwYzAsMzIuNjcsMTguODMsNjEuMTgsNDgsNzYuNDJBODAsODAsMCwwLDAsOTYsMjE2YTgsOCwwLDAsMCwxNiwwLDY0LDY0LDAsMCwxLDEyOCwwLDgsOCwwLDAsMCwxNiwwLDgwLDgwLDAsMCwwLDE2LTE1LjU4Qzk4LjgzLDEyNS4xOCwxMjAsOTYuNjcsMTIwLDY0YTk2LDk2LDAsMCwwLTEwNC0xNkE0MCw0MCwwLDAsMCw4MCw4OGE0MCw0MCwwLDAsMCw4MCwwYzAsMjIuMDktMTYuMzksNDAtMzYuNzMsNDAuMTNBNTcuMDcsNTcuMDcsMCwwLDEsMTM2LDEyMGE0MCw0MCwwLDAsMSw0MC00MCw4LDgsMCwwLDAsMC0xNiw1Niw1NiwwLDAsMC01Niw1Niw4LDgsMCwwLDAsMCwxNiw0MCw0MCwwLDAsMS0yNCwzMloiLz48L3N2Zz4=" alt="Apple Farm Logo">
                <h1>Apple <span>Orchard</span> Paradise</h1>
            </div>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#products">Products</a></li>
                    <li><a href="#visit">Visit Us</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container hero-content">
            <h2>Experience Nature's Sweetest Harvest</h2>
            <p>Family-owned orchard since 1985 - Growing the finest apples in the region</p>
            <a href="#visit" class="btn">Plan Your Visit</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2>Our Story</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Three Generations of Apple Growing</h3>
                    <p>Nestled in the heart of the countryside, Apple Orchard Paradise has been family-owned and operated since 1985. Our passion for growing the finest apples has been passed down through three generations.</p>
                    <p>We practice sustainable farming methods to ensure that our apples are not only delicious but also grown with respect for the environment. Our 100-acre farm features over 20 varieties of apples, each carefully tended to by our experienced team.</p>
                    <p>From crisp Honeycrisp to tart Granny Smith, our apples are hand-picked at the peak of ripeness to ensure the best flavor and texture. We invite you to experience the taste of nature's perfection!</p>
                    <a href="#visit" class="btn">Visit Our Farm</a>
                </div>
                <div class="about-image">
                    <img src="https://images.unsplash.com/photo-1556801363-aa7b8e1b3f7d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=800&q=80" alt="Apple Orchard">
                </div>
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section id="products" class="products">
        <div class="container">
            <div class="section-title">
                <h2>Our Apple Varieties</h2>
            </div>
            <div class="apple-grid">
                <div class="apple-card">
                    <div class="apple-image">
                        <img src="https://images.unsplash.com/photo-1560806887-1e4cd0b6cbd6?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=774&q=80" alt="Honeycrisp Apples">
                    </div>
                    <div class="apple-info">
                        <h3>Honeycrisp</h3>
                        <p>Exceptionally crisp and juicy with a perfect sweet-tart balance</p>
                        <p>Season: September - October</p>
                    </div>
                </div>
                <div class="apple-card">
                    <div class="apple-image">
                        <img src="https://images.unsplash.com/photo-1568702846914-96b305d2aaeb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=870&q=80" alt="Gala Apples">
                    </div>
                    <div class="apple-info">
                        <h3>Gala</h3>
                        <p>Sweet, aromatic and refreshingly crisp</p>
                        <p>Season: August - September</p>
                    </div>
                </div>
                <div class="apple-card">
                    <div class="apple-image">
                        <img src="https://images.unsplash.com/photo-1592492159418-39f319320569?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=870&q=80" alt="Fuji Apples">
                    </div>
                    <div class="apple-info">
                        <h3>Fuji</h3>
                        <p>Super sweet and incredibly crisp with dense flesh</p>
                        <p>Season: October - November</p>
                    </div>
                </div>
                <div class="apple-card">
                    <div class="apple-image">
                        <img src="https://images.unsplash.com/photo-1619546813926-a78fa6372cd2?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=870&q=80" alt="Granny Smith Apples">
                    </div>
                    <div class="apple-info">
                        <h3>Granny Smith</h3>
                        <p>Tart, tangy and delightfully crunchy</p>
                        <p>Season: October - December</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Visit Section -->
    <section id="visit" class="visit">
        <div class="container">
            <div class="section-title">
                <h2>Visit Our Farm</h2>
            </div>
            <div class="visit-content">
                <div class="visit-card">
                    <div class="visit-icon">
                        <i class="fas fa-apple-alt"></i>
                    </div>
                    <h3>Pick Your Own</h3>
                    <p>Experience the joy of picking fresh apples straight from the tree! We provide baskets and guidance to help you find the perfect apples.</p>
                    <p>Open: September 1 - October 31</p>
                    <p>Hours: 9AM - 5PM Daily</p>
                </div>
                <div class="visit-card">
                    <div class="visit-icon">
                        <i class="fas fa-store"></i>
                    </div>
                    <h3>Farm Store</h3>
                    <p>Visit our farm store for fresh-picked apples, homemade cider, apple pies, jams, honey, and other local products.</p>
                    <p>Open Year-Round</p>
                    <p>Hours: 9AM - 6PM Daily</p>
                </div>
                <div class="visit-card">
                    <div class="visit-icon">
                        <i class="fas fa-calendar-alt"></i>
                    </div>
                    <h3>Seasonal Events</h3>
                    <p>Join us for seasonal events including Apple Festivals, Cider Tastings, Harvest Dinners, and Holiday Markets.</p>
                    <p>Check our calendar for upcoming events!</p>
                    <a href="#" class="btn">View Events</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <h2>Get In Touch</h2>
            </div>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Contact Information</h3>
                    <div class="contact-details">
                        <p><i class="fas fa-map-marker-alt"></i> 123 Orchard Lane, Apple Valley, CA 92345</p>
                        <p><i class="fas fa-phone"></i> (555) 123-4567</p>
                        <p><i class="fas fa-envelope"></i> info@appleorchardparadise.com</p>
                        <p><i class="fas fa-clock"></i> Open Daily: 9:00 AM - 6:00 PM</p>
                    </div>
                    <h3>Follow Us</h3>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                    </div>
                </div>
                <div class="contact-form">
                    <h3>Send Us a Message</h3>
                    <form>
                        <div class="form-group">
                            <label for="name">Name</label>
                            <input type="text" id="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" required></textarea>
                        </div>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Apple Orchard Paradise</h3>
                    <p>Growing the finest apples with care and tradition since 1985. Visit us for an unforgettable farm experience!</p>
                </div>
                <div class="footer-column">
                    <h3>Quick Links</h3>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#about">About Us</a></li>
                        <li><a href="#products">Our Apples</a></li>
                        <li><a href="#visit">Plan Your Visit</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Hours</h3>
                    <ul>
                        <li>Monday - Friday: 9AM - 6PM</li>
                        <li>Saturday: 8AM - 7PM</li>
                        <li>Sunday: 9AM - 5PM</li>
                        <li>Holidays: 10AM - 4PM</li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Apple Orchard Paradise. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Header scroll effect
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 100) {
                header.style.backgroundColor = 'rgba(255, 255, 255, 0.98)';
                header.style.boxShadow = '0 2px 15px rgba(0, 0, 0, 0.1)';
            } else {
                header.style.backgroundColor = 'rgba(255, 255, 255, 0.95)';
                header.style.boxShadow = '0 2px 10px rgba(0, 0, 0, 0.1)';
            }
        });

        // Form submission
        const contactForm = document.querySelector('.contact-form form');
        if (contactForm) {
            contactForm.addEventListener('submit', function(e) {
                e.preventDefault();
                alert('Thank you for your message! We will get back to you soon.');
                contactForm.reset();
            });
        }
    </script>
</body>
</html>
