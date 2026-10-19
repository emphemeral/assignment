File 1: index.html (Home Page & Events Table)
Create a new folder for your project. Copy the code below and save it inside the folder as index.html.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Welcome to the Tech Innovators College Club. Discover our activities and upcoming events.">
    <title>Home - Tech Innovators Club</title>
    <link rel="icon" href="images/favicon.ico" type="image/x-icon">
</head>
<body>

    <!-- Consistent Navigation -->
    <header>
        <h1>Tech Innovators Club</h1>
        <nav>
            <a href="index.html">Home</a> | 
            <a href="about.html">About Us</a> | 
            <a href="registration.html">Register</a> | 
            <a href="contact.html">Contact</a>
        </nav>
    </header>

    <hr>

    <main>
        <section>
            <h2>Welcome to Our Club</h2>
            <p>The Tech Innovators Club is a community of students passionate about technology, coding, and building the future. We bridge the gap between classroom theory and real-world application.</p>
        </section>

        <section>
            <h2>What We Do (Club Activities)</h2>
            <ul>
                <li>Weekly Coding Workshops</li>
                <li>Monthly Hackathons</li>
                <li>Guest Tech Speaker Sessions</li>
                <li>Community Outreach & Volunteering</li>
            </ul>
        </section>

        <!-- Information Table: Events Schedule -->
        <section>
            <h2>Upcoming Events Schedule</h2>
            <table border="1" cellspacing="0" cellpadding="8">
                <caption>Fall 2026 Semester Events</caption>
                <thead>
                    <tr>
                        <th>Date</th>
                        <th>Event Name</th>
                        <th>Location</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>October 25, 2026</td>
                        <td>Intro to Web Development</td>
                        <td>Computer Lab 101</td>
                    </tr>
                    <tr>
                        <td>November 5, 2026</td>
                        <td>AI & Ethics Panel</td>
                        <td>Main Auditorium</td>
                    </tr>
                    <tr>
                        <td>November 20, 2026</td>
                        <td>24-Hour Fall Hackathon</td>
                        <td>Student Union Center</td>
                    </tr>
                </tbody>
            </table>
        </section>
    </main>

    <hr>

    <footer>
        <p>&copy; 2026 Tech Innovators Club.</p>
    </footer>

</body>
</html>
File 2: about.html (Club Introduction & Members)
Save this code in the same folder as about.html.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Learn about the history and leadership team of the Tech Innovators Club.">
    <title>About - Tech Innovators Club</title>
    <link rel="icon" href="images/favicon.ico" type="image/x-icon">
</head>
<body>

    <header>
        <h1>Tech Innovators Club</h1>
        <nav>
            <a href="index.html">Home</a> | 
            <a href="about.html">About Us</a> | 
            <a href="registration.html">Register</a> | 
            <a href="contact.html">Contact</a>
        </nav>
    </header>

    <hr>

    <main>
        <section>
            <h2>Our Story</h2>
            <p>Founded in 2022, the Tech Innovators Club started with just five computer science students in a library study room. Today, we have over 100 active members from various majors who come together to build, create, and inspire.</p>
        </section>

        <section>
            <h2>Club Leadership</h2>
            <dl>
                <dt><strong>Jordan Smith - President</strong></dt>
                <dd>Senior CS major with a passion for artificial intelligence and robotics.</dd>

                <dt><strong>Taylor Reed - Vice President</strong></dt>
                <dd>Junior IT major specializing in cybersecurity and network defense.</dd>

                <dt><strong>Alex Chen - Event Coordinator</strong></dt>
                <dd>Sophomore Data Science major who organizes our awesome hackathons.</dd>
            </dl>
        </section>
    </main>

    <hr>

    <footer>
        <p>&copy; 2026 Tech Innovators Club.</p>
    </footer>

</body>
</html>
File 3: registration.html (Registration Form)
Save this code in the same folder as registration.html.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Join the Tech Innovators Club by filling out our student registration form.">
    <title>Register - Tech Innovators Club</title>
    <link rel="icon" href="images/favicon.ico" type="image/x-icon">
</head>
<body>

    <header>
        <h1>Tech Innovators Club</h1>
        <nav>
            <a href="index.html">Home</a> | 
            <a href="about.html">About Us</a> | 
            <a href="registration.html">Register</a> | 
            <a href="contact.html">Contact</a>
        </nav>
    </header>

    <hr>

    <main>
        <h2>Join the Club</h2>
        <p>Ready to start innovating? Fill out the form below to become an official member.</p>

        <form action="#" method="post">
            <div>
                <label for="fullName">Full Name:</label>
                <input type="text" id="fullName" name="fullName" required>
            </div>
            <br>
            
            <div>
                <label for="email">Student Email:</label>
                <input type="email" id="email" name="email" placeholder="you@college.edu" required>
            </div>
            <br>

            <div>
                <label for="major">College Major:</label>
                <input type="text" id="major" name="major" required>
            </div>
            <br>

            <div>
                <label for="gradYear">Expected Graduation Year:</label>
                <input type="number" id="gradYear" name="gradYear" min="2026" max="2032" required>
            </div>
            <br>

            <div>
                <label for="interests">Primary Interest:</label>
                <select id="interests" name="interests">
                    <option value="web">Web Development</option>
                    <option value="ai">Artificial Intelligence</option>
                    <option value="cyber">Cybersecurity</option>
                    <option value="hardware">Hardware/Robotics</option>
                </select>
            </div>
            <br>

            <button type="submit">Submit Registration</button>
        </form>
    </main>

    <hr>

    <footer>
        <p>&copy; 2026 Tech Innovators Club.</p>
    </footer>

</body>
</html>
File 4: contact.html (Contact Information)
Save this code in the same folder as contact.html.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Get in touch with the Tech Innovators Club. Find our location, email, and meeting hours.">
    <title>Contact - Tech Innovators Club</title>
    <link rel="icon" href="images/favicon.ico" type="image/x-icon">
</head>
<body>

    <header>
        <h1>Tech Innovators Club</h1>
        <nav>
            <a href="index.html">Home</a> | 
            <a href="about.html">About Us</a> | 
            <a href="registration.html">Register</a> | 
            <a href="contact.html">Contact</a>
        </nav>
    </header>

    <hr>

    <main>
        <h2>Get In Touch</h2>
        <p>Have questions about the club or want to collaborate? Here is how you can reach us.</p>

        <section>
            <h3>Contact Details</h3>
            <ul>
                <li><strong>Email:</strong> <a href="mailto:hello@techinnovatorsclub.edu">hello@techinnovatorsclub.edu</a></li>
                <li><strong>Phone:</strong> (555) 123-4567</li>
            </ul>
        </section>

        <section>
            <h3>Club Location</h3>
            <p><strong>Address:</strong> Student Union Building, Room 304<br>
            University Campus, City, State 12345</p>
        </section>

        <section>
            <h3>Office Hours</h3>
            <p>Stop by our club room to chat with leadership members!</p>
            <ul>
                <li>Mondays: 2:00 PM - 5:00 PM</li>
                <li>Wednesdays: 2:00 PM - 5:00 PM</li>
                <li>Fridays: 10:00 AM - 1:00 PM</li>
            </ul>
        </section>
    </main>

    <hr>

    <footer>
        <p>&copy; 2026 Tech Innovators Club.</p>
    </footer>

</body>
</html>
Setup and Submission Instructions:
Folder Setup: Ensure all four HTML files (index.html, about.html, registration.html, and contact.html) are saved in the exact same main folder.

Add Your Favicon: Inside that main folder, create an images folder. Place a small icon file inside named favicon.ico so the metadata link (<link rel="icon" href="images/favicon.ico"...>) works correctly.

Test the Site: Double-click index.html to open it in your browser. Click through every link in the navigation bar to ensure you can move freely between all four pages. Make sure your favicon shows up in the browser tab!

Prepare Submission: Compress (zip) your entire main folder and upload it. If your assignment requires a GitHub submission, push the entire folder to a new GitHub repository just as you did in previous assignments.