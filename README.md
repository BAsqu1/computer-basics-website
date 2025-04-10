# computer-basics-website![screen](https://github.com/user-attachments/assets/a1504aa1-1e97-4841-8cee-0ada398d40bf)
![ram](https://github.com/user-attachments/assets/3c9accac-f180-462a-a9f8-5695c1a55242)
![output](https://github.com/user-attachments/assets/d2b5c57c-91d1-43b2-9a8b-ed68dff7c7c2)
![input](https://github.com/user-attachments/assets/924e6887-577b-4907-9fb5-f0083279daeb)
![cpu](https://github.com/user-attachments/assets/d79ab405-4d83-40f5-b324-21f3782abc15)
![screen](https://github.com/user-attachments/assets/2259d459-171a-491f-b0ab-aeacab89ab2a)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Computer Basics - Interactive Learning</title>
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #2980b9;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --text: #333;
        }
        
        * {
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--text);
            background: var(--light);
            margin: 0;
            padding: 0;
        }
        
        .skip-link {
            position: absolute;
            top: -40px;
            left: 0;
            background: var(--accent);
            color: white;
            padding: 8px;
            z-index: 100;
        }
        
        .skip-link:focus {
            top: 0;
        }
        
        header {
            background: var(--primary);
            color: white;
            padding: 2rem;
            text-align: center;
        }
        
        nav {
            background: var(--secondary);
            padding: 1rem;
        }
        
        nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
        }
        
        nav li {
            margin: 0 15px;
        }
        
        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            padding: 5px 10px;
            border-radius: 4px;
            transition: background 0.3s;
        }
        
        nav a:hover, nav a:focus {
            background: rgba(255,255,255,0.2);
            outline: 2px solid white;
        }
        
        main {
            padding: 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        section {
            margin-bottom: 3rem;
            background: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        
        h1 {
            color: white;
            margin: 0;
            font-size: 2.5rem;
        }
        
        h2 {
            color: var(--primary);
            border-bottom: 2px solid var(--secondary);
            padding-bottom: 0.5rem;
            margin-top: 0;
        }
        
        h3 {
            color: var(--accent);
        }
        
        img {
            max-width: 100%;
            height: auto;
            border: 1px solid #ddd;
            border-radius: 4px;
            margin: 1rem 0;
            display: block;
        }
        
        .component-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin: 2rem 0;
        }
        
        .component-card {
            border: 1px solid #ddd;
            border-radius: 8px;
            padding: 1.5rem;
            transition: transform 0.3s;
        }
        
        .component-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .video-container {
            position: relative;
            padding-bottom: 56.25%;
            margin: 2rem 0;
            background: #000;
            border-radius: 8px;
            overflow: hidden;
        }
        
        .video-container iframe {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            border: none;
        }
        
        .transcript {
            background: #f9f9f9;
            padding: 1.5rem;
            border-radius: 4px;
            margin-top: 1rem;
            border-left: 4px solid var(--secondary);
        }
        
        .quiz-form {
            background: white;
            padding: 2rem;
            border-radius: 8px;
        }
        
        fieldset {
            border: 1px solid #ddd;
            border-radius: 4px;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
        }
        
        legend {
            font-weight: bold;
            color: var(--primary);
            padding: 0 10px;
        }
        
        input[type="radio"] {
            margin-right: 10px;
        }
        
        label {
            cursor: pointer;
            display: block;
            margin: 10px 0;
            padding: 8px;
            border-radius: 4px;
        }
        
        label:hover {
            background: #f0f0f0;
        }
        
        button {
            background: var(--accent);
            color: white;
            padding: 12px 24px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: bold;
            transition: background 0.3s;
        }
        
        button:hover, button:focus {
            background: #c0392b;
            outline: 2px solid var(--dark);
        }
        
        footer {
            background: var(--primary);
            color: white;
            text-align: center;
            padding: 2rem;
            margin-top: 2rem;
        }
        
        footer a {
            color: var(--secondary);
        }
        
        @media (max-width: 768px) {
            nav ul {
                flex-direction: column;
                align-items: center;
            }
            
            nav li {
                margin: 5px 0;
            }
            
            main {
                padding: 1rem;
            }
            
            section {
                padding: 1.5rem;
            }
        }
        
        /* Focus styles for keyboard navigation */
        a:focus, button:focus, input:focus {
            outline: 2px solid var(--accent);
            outline-offset: 2px;
        }
    </style>
</head>
<body>
    <a href="#main-content" class="skip-link">Skip to main content</a>
    
    <header>
        <h1>Computer Basics Learning Platform</h1>
    </header>
    
    <nav aria-label="Main navigation">
        <ul>
            <li><a href="#components">Hardware Components</a></li>
            <li><a href="#video">Video Lesson</a></li>
            <li><a href="#quiz">Knowledge Test</a></li>
        </ul>
    </nav>

    <main id="main-content">
        <section id="components">
            <h2>Essential Computer Hardware Components</h2>
            
            <div class="component-grid">
                <div class="component-card" tabindex="0">
                    <h3>CPU (Central Processing Unit)</h3>
                    <img src="images/cpu.jpg" alt="Close-up of a modern CPU chip with metallic surface and pins">
                    <p>The brain of the computer that performs calculations and executes instructions. Modern CPUs have multiple cores for parallel processing.</p>
                </div>
                
                <div class="component-card" tabindex="0">
                    <h3>RAM (Random Access Memory)</h3>
                    <img src="images/ram.jpg" alt="Computer RAM modules with green circuit boards and black chips">
                    <p>Temporary memory that stores data for quick access by the CPU. Volatile memory that clears when power is off.</p>
                </div>
                
                <div class="component-card" tabindex="0">
                    <h3>Storage (HDD/SSD)</h3>
                    <img src="images/storage.jpg" alt="Comparison of HDD and SSD storage devices showing their internal structures">
                    <p>HDDs use spinning disks while SSDs use flash memory. SSDs are faster but more expensive per gigabyte.</p>
                </div>
                
                <div class="component-card" tabindex="0">
                    <h3>Input Devices</h3>
                    <img src="images/input.jpg" alt="Collection of common input devices: keyboard, mouse, and microphone">
                    <p>Devices like keyboards, mice, and microphones that allow users to send data to the computer.</p>
                </div>
                
                <div class="component-card" tabindex="0">
                    <h3>Output Devices</h3>
                    <img src="images/output.jpg" alt="Monitor showing colorful display and a printer producing documents">
                    <p>Monitors, printers, and speakers that display or present data from the computer to the user.</p>
                </div>
            </div>
        </section>

        <section id="video">
            <h2>Video Lesson: How Computers Work</h2>
            
            <div class="video-container">
                <iframe width="560" height="315" src="https://www.youtube.com/embed/mCq8-xTH7jA" title="YouTube video: How Computers Work - Fundamental Concepts" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
            </div>
            
            <div class="transcript">
                <h3>Video Transcript</h3>
                <p>[Narrator] Welcome to this lesson on how computers work. At its core, a computer is a machine that processes information...</p>
                <p>[0:30] The CPU fetches instructions from memory, decodes what they mean, then executes them...</p>
                <p>[1:15] RAM provides fast temporary storage while the computer is running...</p>
                <p>[Full transcript available upon request]</p>
            </div>
        </section>

        <section id="quiz">
            <h2>Test Your Knowledge</h2>
            
            <form class="quiz-form" id="computerQuiz">
                <fieldset>
                    <legend>1. What does CPU stand for?</legend>
                    
                    <label for="q1-a1">
                        <input type="radio" id="q1-a1" name="q1" value="a"> Central Processing Unit
                    </label>
                    
                    <label for="q1-a2">
                        <input type="radio" id="q1-a2" name="q1" value="b"> Computer Processing Unit
                    </label>
                    
                    <label for="q1-a3">
                        <input type="radio" id="q1-a3" name="q1" value="c"> Central Power Unit
                    </label>
                </fieldset>
                
                <fieldset>
                    <legend>2. Which of these is NOT an input device?</legend>
                    
                    <label for="q2-a1">
                        <input type="radio" id="q2-a1" name="q2" value="a"> Keyboard
                    </label>
                    
                    <label for="q2-a2">
                        <input type="radio" id="q2-a2" name="q2" value="b"> Monitor
                    </label>
                    
                    <label for="q2-a3">
                        <input type="radio" id="q2-a3" name="q2" value="c"> Mouse
                    </label>
                </fieldset>
                
                <fieldset>
                    <legend>3. What is the main advantage of SSDs over HDDs?</legend>
                    
                    <label for="q3-a1">
                        <input type="radio" id="q3-a1" name="q3" value="a"> Faster data access
                    </label>
                    
                    <label for="q3-a2">
                        <input type="radio" id="q3-a2" name="q3" value="b"> Lower cost per gigabyte
                    </label>
                    
                    <label for="q3-a3">
                        <input type="radio" id="q3-a3" name="q3" value="c"> Larger storage capacity
                    </label>
                </fieldset>
                
                <button type="submit">Check Your Answers</button>
            </form>
        </section>
    </main>

    <footer>
        <p>© 2023 Computer Basics Learning Platform | Designed with <a href="https://www.w3.org/WAI/standards-guidelines/wcag/" target="_blank">WCAG 2.1</a> accessibility standards</p>
        <p>Contact us at <a href="mailto:info@computer-basics.edu">info@computer-basics.edu</a></p>
    </footer>

    <script>
        // Simple quiz validation
        document.getElementById('computerQuiz').addEventListener('submit', function(e) {
            e.preventDefault();
            let score = 0;
            
            // Check answers
            if (document.querySelector('input[name="q1"]:checked')?.value === 'a') score++;
            if (document.querySelector('input[name="q2"]:checked')?.value === 'b') score++;
            if (document.querySelector('input[name="q3"]:checked')?.value === 'a') score++;
            
            alert(`You scored ${score} out of 3!`);
        });
    </script>
</body>
</html>
