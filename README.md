# portofolio
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ahmad Izza - Portfolio</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
            scroll-behavior: smooth;
        }
        body {
            background-color: #1a1a2e;
            color: #fff;
            text-align: center;
        }
        header {
            background: rgba(0, 0, 0, 0.8);
            padding: 15px 50px;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.3);
            transition: 0.3s ease-in-out;
        }
        header h1 {
            font-size: 24px;
            font-weight: bold;
            color: #00a8ff;
        }
        nav ul {
            list-style: none;
            display: flex;
        }
        nav ul li {
            margin: 0 15px;
        }
        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-size: 16px;
            transition: 0.3s;
        }
        nav ul li a:hover {
            color: #00a8ff;
        }
        section {
            padding: 100px 20px;
            min-height: 80vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            width: 90%;
            margin: auto;
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }
        section.show {
            opacity: 1;
            transform: translateY(0);
        }
        #home {
            height: 100vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background: linear-gradient(to right, #00a8ff, #3b5998);
            width: 100%;
        }
        #home h2 {
            font-size: 40px;
            margin-bottom: 10px;
            animation: fadeIn 1.5s ease-in-out;
        }
        #about, #projects, #contact {
            background: #222;
            padding: 50px;
            border-radius: 10px;
            box-shadow: 0px 2px 10px rgba(0, 0, 0, 0.3);
            width: 100%;
            max-width: 800px;
            margin: 20px auto;
        }
        button {
            background-color: #00a8ff;
            color: white;
            padding: 12px 24px;
            border: none;
            border-radius: 5px;
            font-size: 18px;
            cursor: pointer;
            transition: 0.3s;
        }
        button:hover {
            background-color: #0056b3;
            transform: scale(1.05);
        }
        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(-20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Ahmad Izza</h1>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>
    
    <section id="home" class="show">
        <h2>Welcome to My Portfolio</h2>
        <p>Web Developer & Microsoft Office Specialist</p>
        <button>See My Work</button>
    </section>
    
    <section id="about">
        <h2>About Me</h2>
        <p>Passionate about Web Development and Microsoft Office solutions.</p>
    </section>
    
    <section id="projects">
        <h2>My Projects</h2>
        <p>Coming soon...</p>
    </section>
    
    <section id="contact">
        <h2>Contact Me</h2>
        <p>Email: ahmedizza357@gmail.com</p>
    </section>
    
    <script>
        document.addEventListener("DOMContentLoaded", function() {
            let sections = document.querySelectorAll("section");
            let options = {
                threshold: 0.3
            };
            let observer = new IntersectionObserver((entries, observer) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add("show");
                    }
                });
            }, options);
            sections.forEach(section => {
                observer.observe(section);
            });
        });
    </script>
</body>
</html>
