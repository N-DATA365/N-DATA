
layout: default
title: Home
---

<section id="hero" class="hero">
  <div class="container">
    <h1>Welcome to <span style="color: #1E90FF;">N-DATA</span></h1>
    <p>Your trusted partner in Business Intelligence and Data Visualization</p>
    <a href="/services.html" class="btn">Explore Our Services</a>
  </div>
</section>

<section id="about" class="about">
  <div class="container">
    <h2>About Us</h2>
    <p>We specialize in turning raw data into actionable insights, leveraging advanced tools and techniques to empower businesses.</p>
    <a href="/about.html" class="btn">Learn More</a>
  </div>
</section>
/* General Styles */
body {
  font-family: 'Arial', sans-serif;
  background-color: #000;
  color: #eee;
  margin: 0;
  padding: 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 20px;
}

/* Hero Section */
.hero {
  background: linear-gradient(135deg, #001f3f, #1E90FF);
  color: #fff;
  text-align: center;
  padding: 100px 20px;
}

.hero h1 {
  font-size: 3rem;
  margin-bottom: 10px;
}

.hero p {
  font-size: 1.5rem;
}

.btn {
  background-color: #1E90FF;
  color: #fff;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  text-transform: uppercase;
  cursor: pointer;
}

.btn:hover {
  background-color: #00BFFF;
}
---
layout: default
title: Contact
---

<section class="contact">
  <div class="container">
    <h2>Contact Us</h2>
    <form id="contact-form" action="https://formspree.io/f/{your-endpoint}" method="POST">
      <label for="name">Name:</label>
      <input type="text" id="name" name="name" required>

      <label for="email">Email:</label>
      <input type="email" id="email" name="email" required>

      <label for="message">Message:</label>
      <textarea id="message" name="message" rows="5" required></textarea>

      <button type="submit" class="btn">Send Message</button>
    </form>
  </div>
</section>
// Smooth scrolling for navigation links
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
  anchor.addEventListener('click', function (e) {
    e.preventDefault();
    document.querySelector(this.getAttribute('href')).scrollIntoView({
      behavior: 'smooth'
    });
  });
});

// Contact form submission alert
document.querySelector('#contact-form').addEventListener('submit', (e) => {
  e.preventDefault();
  alert('Thank you for your message! We will get back to you soon.');
});
---
layout: post
title: "Welcome to the N-DATA Blog"
date: 2024-12-04
tags: [Business Intelligence, Data Visualization]
---

Welcome to our blog! This is where we share insights, tips, and the latest trends in Business Intelligence and Data Analytics. Stay tuned for more!
---
layout: default
title: Blog
---

<section class="blog">
  <div class="container">
    <h2>Blog</h2>
    <ul>
      {% for post in site.posts %}
      <li>
        <a href="{{ post.url }}">{{ post.title }}</a>
        <p>{{ post.date | date: "%B %d, %Y" }}</p>
      </li>
      {% endfor %}
    </ul>
  </div>
</section>
<input type="text" id="search-bar" placeholder="Search posts...">
<ul id="search-results"></ul>
const searchBar = document.querySelector('#search-bar');
const resultsList = document.querySelector('#search-results');

searchBar.addEventListener('input', (event) => {
  const query = event.target.value.toLowerCase();
  const results = site.posts.filter(post => 
    post.title.toLowerCase().includes(query) ||
    post.content.toLowerCase().includes(query)
  );
  
  resultsList.innerHTML = results.map(post => `
    <li><a href="${post.url}">${post.title}</a></li>
  `).join('');
});
git add .
git commit -m "Add detailed site structure and code"
git push origin main
