Here is the complete HTML solution for Assignment 3.3. This code meets all the requirements for ordered, unordered, nested, and definition lists, neatly organized into semantic sections.

The HTML Code
Copy the code below and save it on your computer as college-info.html.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>College & Course Information</title>
</head>
<body>

    <!-- 1. Introduction for the college/course -->
    <header>
        <h1>Global Tech University</h1>
        <p>Welcome to Global Tech University, a premier institution dedicated to shaping the future of technology, engineering, and digital innovation. We offer hands-on, practical education to prepare students for the modern workforce.</p>
    </header>

    <hr>

    <!-- 2. Unordered list <ul> for departments -->
    <section>
        <h2>Our Departments</h2>
        <ul>
            <li>Computer Science & Engineering</li>
            <li>Information Technology</li>
            <li>Data Science & Artificial Intelligence</li>
            <li>Cybersecurity</li>
        </ul>
    </section>

    <!-- 4. Nested list for topics of a subject -->
    <section>
        <h2>Course Breakdown: Full-Stack Web Development</h2>
        <p>Here is an overview of what you will learn in our most popular program:</p>
        <ul>
            <li><strong>Frontend Development</strong>
                <ul>
                    <li>HTML5 & Semantic Structure</li>
                    <li>CSS3 Styling & Flexbox/Grid</li>
                    <li>JavaScript Essentials</li>
                </ul>
            </li>
            <li><strong>Backend Development</strong>
                <ul>
                    <li>Node.js & Express</li>
                    <li>RESTful APIs</li>
                    <li>Database Management (SQL/NoSQL)</li>
                </ul>
            </li>
        </ul>
    </section>

    <!-- 3. Ordered list <ol> for the admission process -->
    <section>
        <h2>Admission Process</h2>
        <p>Follow these exact steps to enroll:</p>
        <ol>
            <li>Fill out the online application form on our portal.</li>
            <li>Upload required documents (transcripts and ID).</li>
            <li>Clear the online entrance examination.</li>
            <li>Attend a brief personal interview with the faculty.</li>
            <li>Pay the enrollment fee to secure your seat.</li>
        </ol>
    </section>

    <hr>

    <!-- 5. Description list <dl> for details of teachers/courses -->
    <section>
        <h2>Faculty Directory</h2>
        <dl>
            <dt><strong>Dr. Alan Turing</strong></dt>
            <dd>Head of Computer Science. Specializes in advanced algorithms and artificial intelligence.</dd>

            <dt><strong>Prof. Ada Lovelace</strong></dt>
            <dd>Lead Instructor for Web Development. Has over 15 years of industry experience building scalable applications.</dd>

            <dt><strong>Dr. Tim Berners-Lee</strong></dt>
            <dd>Senior Lecturer for Network Architecture and Web Standards.</dd>
        </dl>
    </section>

</body>
</html>
How to Prepare Your Submission:
Test the File: Double-click your college-info.html file to open it in your web browser (Chrome, Firefox, Safari, etc.).

Review the Lists: Visually verify that you can see standard bullet points (departments), numbered steps (admissions), sub-bullets (nested web development topics), and formatted dictionary-style terms (faculty directory).

Take a Screenshot: While the file is open in your browser, take a clear screenshot showing the rendered lists and headings.

Submit: Upload both your college-info.html file and your screenshot as required by your instructor.