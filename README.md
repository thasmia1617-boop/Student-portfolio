<!DOCTYPE html> 
<html lang=”en”> 
<head> 
    <meta charset=”UTF-8”> 
    <meta name=”viewport” content=”width=device-width, initial-scale=1.0”> 
    <title>Student Portfolio</title> 
    <link rel=”stylesheet” href=”style.css”> 
</head> 
<body> 
<!—Navigation Bar →     <header> 
        <nav class=”navbar”> 
            <div class=”logo”>MyPortfolio</div> 
            <ul class=”nav-links”> 
                <li><a href=”#home”>Home</a></li> 
                <li><a href=”#about”>About</a></li> 
                <li><a href=”#skills”>Skills</a></li> 
                <li><a href=”#projects”>Projects</a></li> 
                <li><a href=”#contact”>Contact</a></li> 
            </ul> 
        </nav> 
    </header> 
 
    <!—Hero Section → 
    <section id=”home” class=”hero”> 
        <div class=”hero-content”> 
            <h1>Hi, I’m <span class=”highlight”>John Doe</span></h1> 
            <p>Computer Science Student & Web Developer</p> 
            <a href=”resume.pdf” class=”btn” download>Download Resume</a> 
        </div> 
    </section> 
 
    <!—About Section → 
    <section id=”about” class=”section”> 
        <h2>About Me</h2> 
        <p>I am a passionate undergraduate student eager to build interactive and responsive web applications using modern web development technologies.</p>     </section> 
 
    <!—Skills Section → 
    <section id=”skills” class=”section bg-light”> 
        <h2>Technical Skills</h2> 
        <div class=”skills-grid”> 
            <div class=”skill-card”>HTML5</div> 
            <div class=”skill-card”>CSS3</div> 
            <div class=”skill-card”>JavaScript</div> 
            <div class=”skill-card”>Git & GitHub</div> 
        </div> 
    </section> 
 
    <!—Projects Section → 
<section id=”projects” class=”section”> 
        <h2>Featured Projects</h2> 
        <div class=”filter-buttons”> 
            <button class=”filter-btn active” data-filter=”all”>All</button> 
            <button class=”filter-btn” data-filter=”web”>Web</button> 
            <button class=”filter-btn” data-filter=”js”>JavaScript</button> 
        </div> 
        <div class=”projects-grid” id=”projects-container”> 
            <!—Dynamically injected via JavaScript → 
        </div> 
    </section> 
 
    <!—Contact Section → 
    <section id=”contact” class=”section bg-light”> 
        <h2>Contact Me</h2> 
        <form id=”contact-form”> 
            <div class=”form-group”> 
                <input type=”text” id=”name” placeholder=”Your Name” required> 
            </div> 
            <div class=”form-group”> 
                <input type=”email” id=”email” placeholder=”Your Email” required> 
            </div> 
            <div class=”form-group”> 
                <textarea id=”message” placeholder=”Your Message” rows=”5” required></textarea> 
            </div> 
            <button type=”submit” class=”btn”>Send Message</button> 
            <p id=”form-feedback”></p> 
        </form> 
    </section> 
 
    <footer> 
        <p>&copy; 2026 Student Portfolio. All rights reserved.</p>     </footer> 
 
    <script src=”script.js”></script> 
</body> 
</html> 
<!DOCTYPE html> 
{ 
Margin: 0; 
    Padding: 0; 
    Box-sizing: border-box; 
    Font-family: ‘Segoe UI’, Tahoma, Geneva, Verdana, sans-serif; 
} 
 
Body { 
    Line-height: 1.6; 
    Color: #333; 
    Scroll-behavior: smooth; 
} 
 
/* Navbar */ 
.navbar { 
    Display: flex; 
    Justify-content: space-between; 
    Align-items: center; 
    Background: #2c3e50; 
    Color: #fff; 
    Padding: 1rem 5%; 
    Position: fixed; 
    Width: 100%;     Top: 0;     z-index: 1000; 
} 
 
.nav-links { 
    List-style: none; 
    Display: flex; 
    Gap: 20px; 
} 
 
.nav-links a { 
    Color: #fff; 
    Text-decoration: none; 
    Transition: color 0.3s; 
} 
 
.nav-links a:hover { 
    Color: #3498db; 
} 
 
/* Hero Section */ 
.hero { 
    Background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url(‘hero-bg.jpg’) norepeat center center/cover; 
    Height: 100vh; 
    Display: flex; 
    Align-items: center; 
    Justify-content: center; 
    Text-align: center; 
    Color: #fff; 
    Padding: 0 20px; 
} 
 
.hero h1 { 
    Font-size: 3rem; 
    Margin-bottom: 10px; 
} 
 
.highlight { 
    Color: #3498db; 
} 
 
.btn { 
    Display: inline-block; 
    Background: #3498db; 
    Color: #fff; 
    Padding: 10px 20px; 
    Border: none; 
    Border-radius: 5px; 
    Text-decoration: none; 
    Margin-top: 15px; 
    Cursor: pointer; 
    Transition: background 0.3s; 
} 
 
.btn:hover { 
    Background: #2980b9; 
} 
 
/* Sections */ 
.section { 
    Padding: 80px 10% 50px; 
    Text-align: center; 
} 
 
.bg-light { 
    Background: #f9f9f9; 
} 
 
.section h2 { 
    Margin-bottom: 40px; 
    Font-size: 2.2rem; 
    Color: #2c3e50; 
} 
 
/* Skills Grid */ 
.skills-grid { 
    Display: grid; 
    Grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); 
    Gap: 20px; 
} 
 
.skill-card { 
    Background: #fff; 
    Padding: 20px; 
    Border-radius: 8px; 
    Box-shadow: 0 2px 5px rgba(0,0,0,0.1); 
    Font-weight: bold; 
    Color: #2c3e50; 
} 
 
/* Projects */ 
.filter-buttons { 
    Margin-bottom: 30px; 
} 
 
.filter-btn { 
    Background: #ddd; 
    Border: none; 
    Padding: 8px 16px;     Margin: 0 5px; 
    Border-radius: 4px; 
    Cursor: pointer; 
    Transition: 0.3s; 
} 
 
.filter-btn.active, .filter-btn:hover { 
    Background: #3498db; 
    Color: #fff; 
} 
 
.projects-grid { 
    Display: grid; 
    Grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); 
    Gap: 20px; 
} 
 
.project-card { 
    Background: #fff; 
    Border-radius: 8px; 
    Padding: 20px; 
    Box-shadow: 0 2px 5px rgba(0,0,0,0.1); 
    Text-align: left; 
} 
 
.project-card h3 { 
    Margin-bottom: 10px; 
    Color: #2c3e50; 
} 
 
/* Contact Form */ 
#contact-form { 
    Max-width: 600px; 
    Margin: 0 auto; 
    Display: flex; 
    Flex-direction: column; 
    Gap: 15px; 
} 
 
.form-group input, .form-group textarea { 
    Width: 100%; 
    Padding: 12px; 
    Border: 1px solid #ccc; 
    Border-radius: 5px; 
} 
 
Footer { 
    Text-align: center; 
    Padding: 20px; 
    Background: #2c3e50; 
    Color: #fff; 
} 
 
// Project Data Array 
Const projects = [ 
    { title: “Portfolio Website”, category: “web”, description: “A responsive personal portfolio built using HTML, CSS, and JS.” }, 
    { title: “Task Manager”, category: “js”, description: “An interactive to-do list application with local storage support.” }, 
    { title: “E-Commerce Landing Page”, category: “web”, description: “A modern product landing page layout designed with CSS Flexbox.” }, 
    { title: “Weather App”, category: “js”, description: “A weather forecast tool fetching real-time data using JavaScript fetch API.” } 
]; 
 
Const projectsContainer = document.getElementById(‘projects-container’); Const filterButtons = document.querySelectorAll(‘.filter-btn’); 
 
// Function to Display Projects 
Function displayProjects(filteredProjects) {     projectsContainer.innerHTML = ‘’;     filteredProjects.forEach(project => {         const card = document.createElement(‘div’);         card.classList.add(‘project-card’);         card.innerHTML = ` 
            <h3>${project.title}</h3> 
            <p>${project.description}</p> 
            <a href=”#” class=”btn”>View Project</a> 
        `; 
        projectsContainer.appendChild(card); 
    }); 
} 
 
// Initial Render displayProjects(projects); 
 
// Filter Event Listeners filterButtons.forEach(button => {     button.addEventListener(‘click’, € => {         document.querySelector(‘.filter-btn.active’).classList.remove(‘active’);         e.target.classList.add(‘active’); 
         
        const filter = e.target.getAttribute(‘data-filter’);         if (filter === ‘all’) {             displayProjects(projects); 
        } else { 
            Const filtered = projects.filter(p => p.category === filter);             displayProjects(filtered); 
        } 
    }); 
}); 
 
// Contact Form Validation Logic 
Const contactForm = document.getElementById(‘contact-form’); 
Const formFeedback = document.getElementById(‘form-feedback’); 
 
contactForm.addEventListener(‘submit’, € => {     e.preventDefault();     const name = document.getElementById(‘name’).value.trim();     const email = document.getElementById(‘email’).value.trim();     const message = document.getElementById(‘message’).value.trim(); 
     
    // Simple Email Regex Validation 
    Const emailPattern = /^[^ ]+@[^ ]+\.[a-z]{2,3}$/; 
 
    If (name === “” || email === “” || message === “”) {         formFeedback.style.color = “red”;         formFeedback.textContent = “Please fill in all mandatory fields.”; 
    } else if (!email.match(emailPattern)) { 
        formFeedback.style.color = “red”;         formFeedback.textContent = “Please enter a valid email address.”; 
    } else {         formFeedback.style.color = “green”;         formFeedback.textContent = “Thank you! Your message has been sent successfully.”; 
        contactForm.reset(); 
    } 
}); 
