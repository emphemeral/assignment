The HTML Code
Copy the code below and save it as job-application.html.

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Job Application Form</title>
</head>
<body>

    <h1>Job Application Form</h1>
    <p>Please fill out the form below to apply for the open position.</p>

    <hr>

    <form action="#" method="post">
        
        <!-- Disabled Field Example -->
        <div>
            <label for="appStatus">Application Status:</label>
            <input type="text" id="appStatus" name="appStatus" value="Draft" disabled>
        </div>
        <br>

        <!-- 1. Full Name, Email, and Phone -->
        <div>
            <label for="fullName">Full Name:</label>
            <input type="text" id="fullName" name="fullName" required>
        </div>
        <br>

        <div>
            <label for="email">Email Address:</label>
            <input type="email" id="email" name="email" required>
        </div>
        <br>

        <div>
            <label for="phone">Phone Number:</label>
            <input type="tel" id="phone" name="phone" required>
        </div>
        <br>

        <!-- 2. Date input for DOB -->
        <div>
            <label for="dob">Date of Birth:</label>
            <input type="date" id="dob" name="dob" required>
        </div>
        <br>

        <!-- 3. URL input for portfolio -->
        <div>
            <label for="portfolio">Portfolio URL:</label>
            <input type="url" id="portfolio" name="portfolio" placeholder="https://..." required>
        </div>
        <br>

        <!-- 6. Dropdown for Job Role -->
        <div>
            <label for="role">Applying For:</label>
            <select id="role" name="role" required>
                <option value="" disabled selected>Select a role...</option>
                <option value="frontend">Front-End Developer</option>
                <option value="backend">Back-End Developer</option>
                <option value="designer">UI/UX Designer</option>
            </select>
        </div>
        <br>

        <!-- 4. Radio buttons for preferred shift -->
        <fieldset>
            <legend>Preferred Shift:</legend>
            <!-- Notice all radio buttons share the name "shift" so only one can be selected -->
            <input type="radio" id="shiftMorning" name="shift" value="morning" required>
            <label for="shiftMorning">Morning</label><br>

            <input type="radio" id="shiftEvening" name="shift" value="evening">
            <label for="shiftEvening">Evening</label><br>

            <input type="radio" id="shiftNight" name="shift" value="night">
            <label for="shiftNight">Night</label>
        </fieldset>
        <br>

        <!-- 5. Checkboxes for skills -->
        <fieldset>
            <legend>Technical Skills (Select all that apply):</legend>
            <input type="checkbox" id="skillHTML" name="skills" value="html">
            <label for="skillHTML">HTML & CSS</label><br>

            <input type="checkbox" id="skillJS" name="skills" value="javascript">
            <label for="skillJS">JavaScript</label><br>

            <input type="checkbox" id="skillGit" name="skills" value="git">
            <label for="skillGit">Git & GitHub</label>
        </fieldset>
        <br>

        <!-- 7. Textarea for Cover Letter -->
        <div>
            <label for="coverLetter">Cover Letter:</label><br>
            <textarea id="coverLetter" name="coverLetter" rows="6" cols="40" placeholder="Tell us why you are a great fit for this role..." required></textarea>
        </div>
        <br>

        <!-- 8. Submit Button -->
        <div>
            <button type="submit">Submit Application</button>
        </div>

    </form>

</body>
</html>
How to Prepare Your Submission:
Test the Form: Double-click your job-application.html file to open it in your browser.

Verify Functionality:

Check that you can only select one preferred shift at a time (because the radio buttons share the same name attribute).

Check that you can select multiple skills.

Notice that the "Application Status" field is greyed out and cannot be typed into (because of the disabled attribute).

Take a Screenshot: Fill in some sample data and take a clear screenshot showing the different input types.

Submit: Upload your job-application.html file and your screenshot according to your course instructions.