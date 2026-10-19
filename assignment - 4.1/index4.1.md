The HTML Code
Copy the code below and save it as registration.html.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Registration Form</title>
</head>
<body>

    <h1>Student Registration</h1>
    <p>Please fill out the form below to register.</p>

    <hr>

    <form action="#" method="post">
        
        <!-- Full Name Field -->
        <div>
            <label for="fullName">Full Name:</label>
            <input type="text" id="fullName" name="fullName" required>
        </div>
        <br>

        <!-- Email Field -->
        <div>
            <label for="email">Email Address:</label>
            <input type="email" id="email" name="email" required>
        </div>
        <br>

        <!-- Password Field -->
        <div>
            <label for="password">Password:</label>
            <input type="password" id="password" name="password" required>
        </div>
        <br>

        <!-- Phone Number Field -->
        <div>
            <label for="phone">Phone Number:</label>
            <input type="tel" id="phone" name="phone" required>
        </div>
        <br>

        <!-- Age Field -->
        <div>
            <label for="age">Age:</label>
            <!-- Using min and max constraints for better data validation -->
            <input type="number" id="age" name="age" min="1" max="120" required>
        </div>
        <br>

        <!-- Submit Button -->
        <div>
            <button type="submit">Register</button>
        </div>

    </form>

</body>
</html>
How to Prepare Your Submission:
Test the Form: Double-click your registration.html file to open it in your web browser.

Verify HTML5 Validation: Try clicking the Register button without filling anything out. The browser should automatically show a warning (like "Please fill out this field") because of the required attribute. Try typing plain text into the Email or Age fields and submitting again—the browser will catch the errors because of the type="email" and type="number" attributes.

Take a Screenshot: Fill out the form with some dummy data and take a clear screenshot of the entire form.

Submit: Upload your registration.html file and your screenshot as instructed by your course.