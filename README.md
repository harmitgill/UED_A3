<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sunshine School</title>
    <link href="https://fonts.googleapis.com/css2?family=Nunito:wght@300;400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Nunito', sans-serif;
            background-color: #F9F1E7;
            color: #4A4A4A;
            margin: 0;
            padding: 0;
        }

        .header {
            background-color: #FFDFD3;
            text-align: center;
            padding: 2rem;
            color: #333;
        }

        .navbar ul {
            list-style: none;
            padding: 0;
            display: flex;
            justify-content: center;
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
            color: #fff;
        }

        .section {
            padding: 3rem 2rem;
            text-align: center;
        }

        .footer {
            background-color: #D4A5A5;
            color: #333;
            text-align: center;
            padding: 1rem;
            font-size: 0.9rem;
        }

        form {
            display: flex;
            flex-direction: column;
            max-width: 400px;
            margin: 2rem auto;
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

        @media (max-width: 768px) {
            .navbar ul {
                flex-direction: column;
            }
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
<section id="home" class="section">
    <h2>Welcome to Sunshine School</h2>
    <p>We are committed to providing a nurturing and enriching learning environment for students of all ages.</p>
</section>

<!-- About Us Section -->
<section id="about" class="section">
    <h2>About Us</h2>
    <p>At Sunshine School, we focus on providing an inclusive and welcoming environment for all students.</p>
</section>

<!-- Academics Section -->
<section id="academics" class="section">
    <h2>Our Academic Programs</h2>
    <p>Explore our comprehensive programs designed for each level of education.</p>
    <div class="academics-links">
        <a href="#primary">Primary Education</a><br>
        <a href="#middle">Middle School</a><br>
        <a href="#high">High School</a>
    </div>
</section>

<!-- Primary School Section -->
<section id="primary" class="section">
    <h2>Primary Education at Sunshine School</h2>
    <p>Our Primary Education program focuses on foundational literacy, numeracy, and creative development for young learners.</p>
</section>

<!-- Middle School Section -->
<section id="middle" class="section">
    <h2>Middle School at Sunshine School</h2>
    <p>The Middle School program helps students develop critical thinking skills, personal responsibility, and teamwork.</p>
</section>

<!-- High School Section -->
<section id="high" class="section">
    <h2>High School at Sunshine School</h2>
    <p>Our High School program prepares students for college and career with challenging coursework and extracurricular opportunities.</p>
</section>

<!-- Gallery Section -->
<section id="gallery" class="section">
    <h2>Gallery</h2>
    <p>Explore images from our school events and activities.</p>
    <div class="gallery">
        <img src="https://via.placeholder.com/300" alt="Event 1">
        <img src="https://via.placeholder.com/300" alt="Event 2">
        <img src="https://via.placeholder.com/300" alt="Event 3">
    </div>
</section>

<!-- Contact Section -->
<section id="contact" class="section">
    <h2>Contact Us</h2>
    <form id="contactForm">
        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required>

        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>

        <label for="message">Message:</label>
        <textarea id="message" name="message" required></textarea>

        <button type="submit">Send Message</button>
    </form>

    <h3>Contact Details</h3>
    <p>Phone: +123 456 7890</p>
    <p>Email: contact@sunshineschool.com</p>
    <p>Address: 123 Sunshine Blvd, City, Country</p>
</section>

<!-- Footer -->
<footer class="footer">
    <p>&copy; 2024 Sunshine School. All Rights Reserved.</p>
</footer>

<script>
    document.getElementById('contactForm').addEventListener('submit', function (event) {
        event.preventDefault();
        const name = document.getElementById('name').value;
        const email = document.getElementById('email').value;
        const message = document.getElementById('message').value;
        document.getElementById('formResponse').textContent = `Thank you, ${name}! Your message has been sent.`;
        document.getElementById('contactForm').reset();
    });
</script>

</body>
</html>
