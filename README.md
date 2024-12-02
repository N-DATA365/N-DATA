# N-DATA
A website for data analysis and interactive reports


<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>N-DATA - Data Analysis</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <div class="navbar">
            <a href="#">Home</a>
            <a href="#services">Services</a>
            <a href="#about">About</a>
            <a href="#contact">Contact</a>
        </div>
    </header>

    <section id="home">
        <h1>Welcome to N-DATA</h1>
        <p>We specialize in data analysis and deliver actionable insights.</p>
    </section>

    <section id="services">
        <h2>Our Services</h2>
        <div class="service">
            <h3>Big Data Analysis</h3>
            <p>We help businesses handle and analyze large datasets efficiently.</p>
        </div>
        <div class="service">
            <h3>Interactive Reports</h3>
            <p>We provide interactive dashboards with tools like Power BI.</p>
        </div>
    </section>

    <section id="about">
        <h2>About N-DATA</h2>
        <p>We are a team of data experts offering innovative solutions to businesses worldwide.</p>
    </section>

    <section id="contact">
        <h2>Contact Us</h2>
        <form>
            <label for="name">Name:</label>
            <input type="text" id="name" name="name">
            
            <label for="email">Email:</label>
            <input type="email" id="email" name="email">

            <label for="message">Message:</label>
            <textarea id="message" name="message"></textarea>

            <button type="submit">Send</button>
        </form>
    </section>

    <footer>
        <p>&copy; 2024 N-DATA. All rights reserved.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>

document.querySelector("form").addEventListener("submit", function(event) {
    event.preventDefault();
    alert("Your message has been sent!");
});

body {
    font-family: 'Arial', sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: white;
    padding: 10px 0;
    text-align: center;
}

.navbar a {
    margin: 0 15px;
    color: white;
    text-decoration: none;
    font-weight: bold;
}

h1, h2 {
    text-align: center;
    margin-top: 20px;
}

section {
    padding: 20px;
    margin: 20px 0;
}

footer {
    text-align: center;
    background-color: #333;
    color: white;
    padding: 10px;
}
