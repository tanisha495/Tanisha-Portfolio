<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tanisha Khanna</title>
    <style>
        :root {
            --bg-color: #f4f4f9;
            --text-color: #333;
            --section-bg-color: #fff;
            --footer-bg-color: #333;
            --footer-text-color: #fff;
            --link-color: #024cf9;
        }

        [data-theme="dark"] {
            --bg-color: #121212;
            --text-color: #f4f4f9;
            --section-bg-color: #1e1e1e;
            --footer-bg-color: #ffffff;
            --footer-text-color: #333;
            --link-color: #90caf9;
        }

        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            line-height: 1.6;
            background-color: var(--bg-color);
            color: var(--text-color);
            transition: background-color 0.3s, color 0.3s;
        }

        header {
            background: var(--footer-bg-color);
            color: var(--footer-text-color);
            padding: 30px 20px;
            text-align: center;
            position: relative;
            border-radius: 0 0 30px 30px;
        }

        .photo-section {
            position: absolute;
            top: 20px;
            right: 30px;
            width: 110px;
            height: 110px;
            border-radius: 50%;
            overflow: hidden;
            border: 2px solid var(--footer-text-color);
        }

        .photo-section img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .theme-toggle {
            position: fixed;
            bottom: 10px;
            right: 20px;
            background: var(--section-bg-color);
            border: 2px solid var(--text-color);
            padding: 10px;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px; 
            cursor: pointer;
            color: var(--text-color);
            transition: background-color 0.3s, color 0.3s,transform 0.2s;
            z-index: 1000;
        }

        .theme-toggle:hover {
            transform: scale(1.1);
        }

        section {
            margin: 20px;
            padding: 20px;
            background: var(--section-bg-color);
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            transition: background-color 0.3s, box-shadow 0.3s;
        }

        h2 {
            border-bottom: 2px solid var(--bg-color);
            padding-bottom: 5px;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin: 10px 0;
        }

        table th, table td {
            border: 1px solid var(--bg-color);
            padding: 10px;
            text-align: left;
        }

        table th {
            background-color: var(--bg-color);
        }

        footer {
            background: var(--footer-bg-color);
            color: var(--footer-text-color);
            text-align: center;
            padding: 20px;
            border-radius: 30px 30px 0 0;
        }

        footer a {
            color: var(--link-color);
            text-decoration: none;
            margin: 0 10px;
        }

        footer a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>
    <button class="theme-toggle" onclick="toggleTheme()">
        <span id="theme-icon">🌙</span>
    </button>

    <header>
        <h1>TANISHA KHANNA</h1>
        <div class="photo-section">
            <img src="IMG_1198.jpeg" alt="My Photo">
        </div>
    </header>

    <section id="about-me">
        <h2>About Me</h2>
        <p>Hello! I am a first-year BTech student passionate about technology and AI. I am currently working on a research paper about AI in Radiology in breast cancer prognosis as part of the ACM student chapter.</p>
    </section>

    <section id="qualifications">
        <h2>Qualifications</h2>
        <table>
            <thead>
                <tr>
                    <th>Degree</th>
                    <th>Institution</th>
                    <th>Year</th>
                    <th>Grade/Percentage</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>BTech in Computer Science and Engineering</td>
                    <td>Indira Gandhi Delhi Technical University for Women</td>
                    <td>First year - Present</td>
                    <td>-</td>
                </tr>
                <tr>
                    <td>Higher Secondary (12th Grade)</td>
                    <td>St. Michaels's Sr. Sec. School</td>
                    <td>2023</td>
                    <td>94.6</td>
                </tr>
                <tr>
                    <td>Secondary School (10th Grade)</td>
                    <td>St. Michaels's Sr. Sec. School</td>
                    <td>2021</td>
                    <td>94.4</td>
                </tr>
            </tbody>
        </table>
    </section>

    <section id="programming-languages">
        <h2>Programming Languages I Know</h2>
        <ul>
            <li>Python</li>
            <li>C</li>
            <li>JavaScript</li>
        </ul>
    </section>

    <section id="databases">
        <h2>Databases I Know</h2>
        <ul>
            <li>MySQL</li>
            <li>PostgreSQL</li>
            <li>MongoDB</li>
        </ul>
    </section>

    <section id="achievements">
        <h2>Achievements</h2>
        <ul>
            <li>Research paper mentee in ACM student chapter</li>
        </ul>
    </section>

    <section id="hobbies">
        <h2>Hobbies</h2>
        <ul>
            <li>Coding</li>
            <li>Playing Basketball</li>
            <li>Gaming</li>
        </ul>
    </section>

    <footer>
        <p>Contact Me:</p>
        <p>
            <a href="www.linkedin.com/in/tanisha-khanna-432672323" target="_blank">LinkedIn</a> |
            <a href="https://github.com/tanisha495" target="_blank">GitHub</a> |
            <a href="mailto:tanisha.khanna2022@gmail.com">Email</a> |
            <span>Mobile: +91 9811338052</span>
        </p>
    </footer>

    <script>
        function toggleTheme() {
            const body = document.body;
    const themeIcon = document.getElementById('theme-icon');
    const currentTheme = body.getAttribute('data-theme');
    const newTheme = currentTheme === 'dark' ? 'light' : 'dark';

    body.setAttribute('data-theme', newTheme);

    themeIcon.textContent = newTheme === 'dark' ? '☀️' : '🌙';
        }

        
        document.body.setAttribute('data-theme', 'light');
    </script>
</body>
</html>
