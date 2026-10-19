The HTML Code
Copy the code below and save it as marksheet.html.

(Note: The border, cellspacing, and cellpadding attributes are used here so you can visually see the table grid without needing to write any CSS.)

HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Marksheet</title>
</head>
<body>

    <h1>End of Semester Results</h1>
    <p>Below is the detailed marksheet for the current class.</p>

    <hr>

    <table border="1" cellspacing="0" cellpadding="8">
        
        <!-- 4. Title of the table -->
        <caption>Student Marksheet - Fall 2026</caption>
        
        <!-- 3. Table Header -->
        <thead>
            <tr>
                <!-- 6. Using rowspan for the name and total columns to span across the two header rows -->
                <th rowspan="2">Student Name</th>
                
                <!-- 6. Using colspan to group the subjects together -->
                <th colspan="3">Subjects (Out of 100)</th>
                
                <th rowspan="2">Total Marks</th>
            </tr>
            <tr>
                <!-- 7. Meaningful headers for the specific subjects -->
                <th>Mathematics</th>
                <th>Science</th>
                <th>English</th>
            </tr>
        </thead>
        
        <!-- 3. Table Body with data for 5 students and 3 subjects -->
        <tbody>
            <tr>
                <td>Alice Johnson</td>
                <td>85</td>
                <td>90</td>
                <td>88</td>
                <td>263</td>
            </tr>
            <tr>
                <td>Bob Smith</td>
                <td>78</td>
                <td>82</td>
                <td>80</td>
                <td>240</td>
            </tr>
            <tr>
                <td>Charlie Davis</td>
                <td>92</td>
                <td>88</td>
                <td>95</td>
                <td>275</td>
            </tr>
            <tr>
                <td>Diana Prince</td>
                <td>88</td>
                <td>94</td>
                <td>89</td>
                <td>271</td>
            </tr>
            <tr>
                <td>Ethan Hunt</td>
                <td>76</td>
                <td>70</td>
                <td>82</td>
                <td>228</td>
            </tr>
        </tbody>
        
        <!-- 3. Table Footer -->
        <tfoot>
            <tr>
                <!-- 5. Showing average marks in the footer, using colspan to push the number to the far right -->
                <th colspan="4" align="right">Overall Class Average Total:</th>
                <th>255.4</th>
            </tr>
        </tfoot>

    </table>

</body>
</html>
How to Prepare Your Submission:
Test the Table: Double-click your marksheet.html file to open it in your web browser.

Verify Spans: Look closely at the top headers. "Subjects (Out of 100)" should stretch nicely across the three specific class names (colspan), while "Student Name" and "Total Marks" should stretch downward to fill the empty vertical space (rowspan).

Take a Screenshot: Ensure the entire table, including the caption at the top and the footer at the bottom, is visible on your screen, and take a clear screenshot.

Submit: Upload your marksheet.html file and your screenshot according to your course instructions.