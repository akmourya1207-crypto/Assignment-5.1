Here is the complete solution for Assignment 5.1 — Convert an HTML Page into a Styled Page.

To complete this assignment, you will create two files in the same folder on your computer: index.html and style.css.

1. The HTML File (index.html)
Save this code as index.html. Notice Step 2: the external stylesheet is linked in the <head> section using <link rel="stylesheet" href="style.css">.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Portal & Registration</title>
    <!-- Step 2: Link the external stylesheet -->
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <!-- Header & Navigation (Step 5) -->
    <header>
        <div class="logo">🎓 Campus Portal</div>
        <nav aria-label="Main Navigation">
            <a href="#home">Home</a>
            <a href="#about">About</a>
            <a href="#register">Register</a>
        </nav>
    </header>

    <!-- Main Content Area -->
    <main>
        <section id="home">
            <h1>Welcome to Student Portal</h1>
            <p>Your centralized hub for course registration, academic resources, and campus updates. Designed to make your academic journey smooth, modern, and fully accessible.</p>
            <a href="#register" class="btn">Get Started</a>
        </section>

        <section id="about">
            <h2>About Our Platform</h2>
            <p>Our student portal connects you with top-tier faculty, comprehensive course materials, and streamlined administrative workflows. We prioritize clean design, readability, and effortless navigation.</p>
        </section>

        <section id="register">
            <h2>Student Registration Form</h2>
            <form action="#" method="POST">
                <div class="form-group">
                    <label for="fullname">Full Name</label>
                    <input type="text" id="fullname" name="fullname" placeholder="Enter your full name" required>
                </div>

                <div class="form-group">
                    <label for="email">Email Address</label>
                    <input type="email" id="email" name="email" placeholder="student@example.com" required>
                </div>

                <div class="form-group">
                    <label for="course">Preferred Course</label>
                    <select id="course" name="course" required>
                        <option value="" disabled selected>Select a course</option>
                        <option value="web">Web Development & Design</option>
                        <option value="data">Data Structures & Algorithms</option>
                        <option value="database">Database Management Systems</option>
                    </select>
                </div>

                <button type="submit" class="submit-btn">Register Now</button>
            </form>
        </section>
    </main>

    <footer>
        <p>&copy; 2026 Campus Portal. All rights reserved.</p>
    </footer>

</body>
</html>
2. The CSS File (style.css)
Save this code as style.css in the exact same folder as your index.html file.

CSS
/* Step 3: Set body background, text color, and font */
body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background-color: #f4f7f6;
    color: #333333;
    margin: 0;
    padding: 0;
    line-height: 1.6;
}

/* Header & Navigation Layout (Step 5) */
header {
    background-color: #1a2a3a;
    color: #ffffff;
    padding: 1rem 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    position: sticky;
    top: 0;
    z-index: 1000;
}

.logo {
    font-size: 1.4rem;
    font-weight: bold;
    letter-spacing: 0.5px;
}

nav {
    display: flex;
    gap: 15px;
}

/* Step 5: Make navigation links readable and attractive */
nav a {
    color: #ffffff;
    text-decoration: none;
    font-weight: 600;
    padding: 6px 14px;
    border-radius: 4px;
    transition: background-color 0.2s ease, color 0.2s ease;
}

nav a:hover, nav a:focus {
    background-color: #0066cc;
    color: #ffffff;
    outline: none;
}

/* Main Container & Sections */
main {
    max-width: 800px;
    margin: 40px auto;
    padding: 0 20px;
}

section {
    background-color: #ffffff;
    padding: 30px;
    margin-bottom: 30px;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
}

/* Step 4: Style headings */
h1, h2 {
    color: #1a2a3a;
    margin-top: 0;
}

h1 {
    font-size: 2.2rem;
    margin-bottom: 15px;
}

h2 {
    font-size: 1.5rem;
    border-bottom: 2px solid #0066cc;
    padding-bottom: 8px;
    margin-bottom: 20px;
}

/* Step 4: Style paragraphs */
p {
    color: #555555;
    font-size: 1rem;
    margin-bottom: 20px;
}

/* Step 4: Style general links */
a {
    color: #0066cc;
    text-decoration: none;
}

a:hover {
    text-decoration: underline;
}

/* Buttons & Form Elements */
.btn, .submit-btn {
    display: inline-block;
    background-color: #0066cc;
    color: #ffffff;
    padding: 10px 20px;
    border-radius: 4px;
    font-weight: bold;
    border: none;
    cursor: pointer;
    text-decoration: none;
    transition: background-color 0.2s ease;
}

.btn:hover, .submit-btn:hover {
    background-color: #004b99;
    text-decoration: none;
}

.form-group {
    margin-bottom: 18px;
}

label {
    display: block;
    font-weight: bold;
    margin-bottom: 6px;
    color: #333333;
}

input, select {
    width: 100%;
    padding: 10px 12px;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-size: 14px;
    box-sizing: border-box;
}

input:focus, select:focus {
    border-color: #0066cc;
    outline: none;
}

.submit-btn {
    width: 100%;
    margin-top: 10px;
}

/* Footer */
footer {
    background-color: #1a2a3a;
    color: #ffffff;
    text-align: center;
    padding: 20px;
    margin-top: 40px;
    font-size: 0.9rem;
}
Step 6: How to Inspect Styles Using Chrome DevTools
Open your index.html file in Google Chrome.

Right-click anywhere on the webpage (such as the navigation bar or heading) and select Inspect (or press Ctrl+Shift+I on Windows / Cmd+Option+I on Mac).

In the DevTools panel that opens:

Use the Elements tab to select HTML elements and view how your CSS rules apply in the Styles sub-pane on the right.

Use the Console or Network tabs to verify that style.css loaded successfully with a 200 OK status.