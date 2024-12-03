<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sunshine Primary School</title>

    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Nunito:wght@300;400;700&display=swap" rel="stylesheet">

    <!-- Swiper.js CSS for Carousel -->
    <link rel="stylesheet" href="https://unpkg.com/swiper/swiper-bundle.min.css">

    <!-- AOS CSS for Scroll Animations -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.css" />

    <!-- Internal CSS -->
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Nunito', sans-serif;
            background-color: #F9F1E7;
            color: #4A4A4A;
        }

        .header {
            background-color: #FFDFD3;
            text-align: center;
            padding: 2rem;
            color: #333;
        }

        .navbar ul {
            display: flex;
            justify-content: center;
            list-style: none;
            gap: 1rem;
        }

        .navbar a {
            color: #333;
            text-decoration: none;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            transition: background-color 0.3s;
        }

        .navbar a:hover {
            background-color: #F7B8A0;
            color: white;
        }

        .section {
            padding: 3rem 2rem;
            text-align: center;
        }

        .section img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
        }

        /* Swiper Gallery Styles */
        .swiper-container {
            width: 100%;
            margin: 0 auto;
        }

        .swiper-slide img {
            border-radius: 10px;
            width: 100%;
            height: auto;
        }

        .swiper-button-next,
        .swiper-button-prev {
            color: #FF9D7B;
        }

        .swiper-pagination-bullet {
            background-color: #FF9D7B;
        }

        /* Modal for Image Lightbox */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            background-color: rgba(0, 0, 0, 0.8);
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            justify-content: center;
            align-items: center;
        }

        .modal img {
            max-width: 80%;
            margin: 5% auto;
            display: block;
        }

        .close-modal {
            position: absolute;
            top: 10px;
            right: 20px;
            font-size: 2rem;
            color: white;
            cursor: pointer;
        }

        /* Form Styling */
        form {
            display: flex;
            flex-direction: column;
            max-width: 500px;
            margin: 0 auto;
            padding: 1rem;
            background-color: #fff;
            border-radius: 5px;
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.1);
        }

        input, textarea, button {
            margin: 0.5rem 0;
            padding: 0.7rem;
            border-radius: 5px;
            border: 1px solid #ddd;
        }

        button {
            background-color: #FFB6A9;
            color: #fff;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        button:hover {
            background-color: #FF9D7B;
        }

        /* Footer Styling */
        .footer {
            background-color: #D4A5A5;
            text-align: center;
            padding: 1rem;
        }

    </style>
</head>
<body>

    <!-- Header -->
    <header class="header">
        <h1>Sunshine School</h1>
        <p>Building Bright Futures Together</p>
        <nav class="navbar">
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About Us</a></li>
                <li><a href="#academics">Academics</a></li>
                <li><a href="#gallery">Gallery</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- Home Section -->
    <section id="home" class="section" data-aos="fade-up">
        <h2>Welcome to Sunshine School!</h2>
        <p>Sunshine School nurtures a joyful and inspiring environment for young learners.</p>
        <img src="https://source.unsplash.com/600x300/?school-campus" alt="School Campus">
    </section>

    <!-- About Us Section -->
    <section id="about" class="section" data-aos="fade-up">
        <h2>About Us</h2>
        <p>At Sunshine School, we focus on nurturing each child’s unique abilities. Our experienced staff is dedicated to supporting the academic, social, and emotional growth of every student.</p>
        <img src="https://source.unsplash.com/600x300/?classroom" alt="Classroom Activity">
    </section>

    <!-- Academics Section -->
    <section id="academics" class="section" data-aos="fade-up">
        <h2>Academics</h2>
        <p>Our school offers a rich curriculum designed to challenge and inspire students. We offer programs in the following areas:</p>
        <ul>
            <li><strong>Primary Education</strong>: Foundational skills in reading, math, and science.</li>
            <li><strong>Middle School</strong>: Preparing students for high school with advanced subjects and enrichment programs.</li>
            <li><strong>High School</strong>: Preparing students for college and beyond, offering a broad range of academic and extracurricular activities.</li>
        </ul>
        <img src="https://source.unsplash.com/600x300/?school-education" alt="Academics Program">
    </section>

    <!-- Gallery Section -->
    <section id="gallery" class="section" data-aos="fade-up">
        <h2>Gallery</h2>
        <p>Explore our school activities below.</p>

        <!-- Swiper Gallery -->
        <div class="swiper-container">
            <div class="swiper-wrapper">
                <div class="swiper-slide">
                    <img src="https://source.unsplash.com/600x300/?sports" alt="Sports Event" onclick="openModal(this)">
                </div>
                <div class="swiper-slide">
                    <img src="https://source.unsplash.com/600x300/?art" alt="Art Activity" onclick="openModal(this)">
                </div>
                <div class="swiper-slide">
                    <img src="https://source.unsplash.com/600x300/?science" alt="Science Fair" onclick="openModal(this)">
                </div>
            </div>

            <!-- Swiper Navigation Buttons -->
            <div class="swiper-button-next"></div>
            <div class="swiper-button-prev"></div>

            <!-- Swiper Pagination -->
            <div class="swiper-pagination"></div>
        </div>

        <!-- Modal for Image Lightbox -->
        <div class="modal" id="imageModal">
            <span class="close-modal" id="closeModal">&times;</span>
            <img id="modalImage" src="" alt="Large View">
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="section" data-aos="fade-up">
        <h2>Contact Us</h2>
        <p>Have questions? Reach out to us via the contact form or directly at:</p>
        <p>Phone: (123) 456-7890 | Email: contact@sunshineschool.com</p>
        <p><strong>Address:</strong> 123 Main Street, Springfield, IL 62701</p>

        <form id="contactForm">
            <input type="text" id="name" placeholder="Your Name" required>
            <input type="email" id="email" placeholder="Your Email" required>
            <textarea id="message" placeholder="Your Message" required></textarea>
            <button type="submit">Send Message</button>
        </form>
    </section>

    <!-- Footer -->
    <footer class="footer">
        <p>&copy; 2024 Sunshine School. All Rights Reserved.</p>
    </footer>

    <!-- Scripts -->
    <script src="https://unpkg.com/swiper/swiper-bundle.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.js"></script>

    <script>
        // Initialize AOS for Scroll Animations
        AOS.init();

        // Initialize Swiper for Gallery
        const swiper = new Swiper('.swiper-container', {
            loop: true,
            slidesPerView: 1,
            spaceBetween: 10,
            navigation: {
                nextEl: '.swiper-button-next',
                prevEl: '.swiper-button-prev'
            },
            pagination: {
                el: '.swiper-pagination',
                clickable: true
            }
        });

        // Modal Image Gallery
        const modal = document.getElementById('imageModal');
        const modalImage = document.getElementById('modalImage');
        const closeModal = document.getElementById('closeModal');

        function openModal(image) {
            modal.style.display = 'flex';
            modalImage.src = image.src;
        }

        closeModal.addEventListener('click', () => {
            modal.style.display = 'none';
        });

        // Contact Form Submission
        document.getElementById('contactForm').addEventListener('submit', function(event) {
            event.preventDefault();
            const name = document.getElementById('name').value;
            alert(`Thank you, ${name}! Your message has been sent.`);
            this.reset();
        });
    </script>

</body>
</html>
