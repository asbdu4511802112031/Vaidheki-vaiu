<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio</title>
    <style>
        /* General Styles */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            text-align: center;
            background-color: #f4f4f4;
        }

        /* Header */
        header {
            background: black;
            color: white;
            padding: 15px;
        }

        nav ul {
            list-style: none;
            padding: 0;
        }

        nav ul li {
            display: inline;
            margin: 0 15px;
        }

        nav ul li a {
            color: white;
            text-decoration: none;
        }

        /* Sections */
        section {
            padding: 50px;
        }

        /* About Section */
        #about img {
            width: 150px;
            border-radius: 50%;
            margin-top: 10px;
        }

        /* Projects */
        .project {
            background: white;
            padding: 20px;
            margin: 20px auto;
            width: 60%;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        /* Contact Form */
        form {
            display: flex;
            flex-direction: column;
            width: 50%;
            margin: auto;
        }

        input, textarea, button {
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        button {
            background: #28a745;
            color: white;
            cursor: pointer;
        }

        button:hover {
            background: #218838;
        }
    </style>
</head>
<body>

    <!-- Header / Navigation -->
    <header>
        <h1>My Portfolio</h1>
        <nav>
            <ul>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <!-- About Section -->
    <section id="about">
        <h2>About Me</h2>
        <p>Hello! I am [Your Name], a passionate web developer.</p>
        <img src="profile.jpg" alt="Profile Picture">
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <h2>My Projects</h2>
        <div class="project">
            <h3>Project 1</h3>
            <p>Description of my project.</p>
        </div>
        <div class="project">
            <h3>Project 2</h3>
            <p>Another project I worked on.</p>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <h2>Contact Me</h2>
        <form id="contactForm">
            <input type="text" id="name" placeholder="Your Name" required>
            <input type="email" id="email" placeholder="Your Email" required>
            <textarea id="message" placeholder="Your Message" required></textarea>
            <button type="submit">Send</button>
        </form>
        <p id="responseMessage"></p>
    </section>

    <script>
        // JavaScript to handle form submission
        document.getElementById("contactForm").addEventListener("submit", function(event) {
            event.preventDefault(); // Prevent form from refreshing the page

            let name = document.getElementById("name").value;
            let email = document.getElementById("email").value;
            let message = document.getElementById("message").value;

            if (name === "" || email === "" || message === "") {
                alert("Please fill in all fields!");
                return;
            }

            document.getElementById("responseMessage").innerText = `Thank you, ${name}! I'll get back to you soon.`;

            // Clear form fields
            document.getElementById("contactForm").reset();
        });
    </script>

</body>
</html>
