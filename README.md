```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Portfolio</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        /* Navbar style */
        .navbar {
            transition: transform 0.3s ease-out;
        }

        .navbar.hidden {
            transform: translateY(-100%);
        }

        /* Card style */
        .card {
                transition: all 0.3s ease;
                cursor: pointer;
        }

        .card:hover {
            animation: shake 0.5s;
        }

        .middle-card {
            transform: scale(1.1);
            box-shadow: 0 10px 20px rgba(0,0,0,0.2);
            z-index: 1;
        }

        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            25% { transform: translateX(-5px); }
            75% { transform: translateX(5px); }
        }

        /* Colors */
        :root {
            --bs-primary: #4499cc;
            --bs-primary-rgb: 68, 153, 204;
        }

        .progress-bar {
            background: var(--gradient) !important;
        }
        
        /* Kotlin progress bar */
        .Kotlin {
            --gradient: linear-gradient(45deg, #8A2BE2, #9932CC, #9370DB);
        }
        
        /* Compose progress bar */
        .Compose {
            --gradient: linear-gradient(45deg, #50C878, #3CB371, #98FB98);
        }
        
        /* JavaScript progress bar */
        .Javascript {
            --gradient: linear-gradient(45deg, #FFD700, #FFA500, #DAA520);
        }
        
        /* React progress bar */
        .React {
            --gradient: linear-gradient(45deg, #4169E1, #1E90FF, #87CEEB);
        }

        .btn-primary {
            --bs-btn-bg: #4499cc;
            --bs-btn-border-color: #4499cc;
            --bs-btn-hover-bg: #6699cc;
            --bs-btn-hover-border-color: #6699cc;
        }

        .bg-dark {
            --bs-dark-rgb: 42, 42, 42;
        }

        #projects, #skills, #contact {
            background-color: rgba(var(--bs-primary-rgb), 0.1) !important;
        }

        .card:hover {
            background: linear-gradient(45deg, #4499cc, #6699cc, #99ccff);
            color: var(--bs-white);
        }

        .project-card {
            border-color: var(--bs-primary);
        }

        .project-card:hover .card-title {
            background: linear-gradient(45deg, #4499cc, #6699cc, #99ccff);
            -webkit-background-clip: text;
            background-clip: text;
            -webkit-text-fill-color: white;
        }

        .project-card img {
            transition: all 0.3s ease;
        }

        .project-card:hover img {
            filter: brightness(1.2);
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark fixed-top" id="mainNav">
        <div class="container">
            <a class="navbar-brand" href="#">
                <h5>Welcome to <span style="background: linear-gradient(45deg, #66ccff, #99ccff, #ccffff); background-clip: text; -webkit-background-clip: text; background-clip: text; -webkit-text-fill-color: transparent;">Dario's</span> Portfolio</h5>
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="#intro">About</a></li>
                    <li class="nav-item"><a class="nav-link" href="#projects">Projects</a></li>
                    <li class="nav-item"><a class="nav-link" href="#skills">Skills</a></li>
                    <li class="nav-item"><a class="nav-link" href="#contact">Contact</a></li>
                </ul>
            </div>
        </div>
    </nav>

    <!-- Introduction Section -->
    <section id="intro" class="py-5 pt-5" style="background-image: url('https://i.gifer.com/J4o.gif'); background-size: cover; background-position: center; background-attachment: fixed;">
        <div class="container text-center col justify-content-center pt-5">
            <div class="row align-items-center justify-content-center g-0">
                <div class="col-auto text-end pt-3">
                    <h2 class="text-white">Web</h2>
                    <h2 class="text-white">Developer</h2>
                </div>
                <div class="col-auto">
                    <span class="display-1 my-4" style="background: linear-gradient(45deg, #66ccff, #99ccff, #ccffff); -webkit-background-clip: text; background-clip: text; -webkit-text-fill-color: transparent; font-stretch: ultra-condensed; transform: scale(0.5, 1);">&</span>
                </div>
                <div class="col-auto text-start pt-3">
                    <h2 class="text-white">Android</h2>
                    <h2 class="text-white">Designer</h2>
                </div>
            </div>
            <h3 class="text-white mt-5">I am a passionate web developer with experience in creating responsive and user-friendly applications</h3>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="py-5 bg-light">
        <div class="container">
            <h2 class="text-center mb-4">My Projects</h2>

            <div class="row justify-content-center g-5" id="projectCards">
                <div class="col-md-4 mb-4">
                    <div class="card project-card" onclick="moveToMiddle(0)">
                        <img src="./WeFind.png" class="card-img-top" alt="Project 1" style="height: 200px; object-fit: cover;">
                        <div class="card-body">
                            <h5 class="card-title">We<span style="color: green;">Find</span></h5>
                            <p class="card-text">This website allows you check most of the touristic rental available in Mallorca.  The information displayed in this website has been obtained from the Goverment's official touristic information.</p>
                        </div>
                    </div>
                </div>
                <div class="col-md-4 mb-4">
                    <div class="card project-card middle-card" onclick="moveToMiddle(1)">
                        <img src="./BStores.png" class="card-img-top" alt="Project 2" style="height: 200px; object-fit: cover;">
                        <div class="card-body">
                            <h5 class="card-title">B<span style="color: gold;">S</span>tores</h5>
                            <p class="card-text">This Android app allows you to manage business inventory and track sales, expenses, and profits in real-time. Features include barcode scanning, inventory alerts, and financial reporting.</p>
                        </div>
                    </div>
                </div>
                <div class="col-md-4 mb-4">
                    <div class="card project-card" onclick="moveToMiddle(2)">
                        <img src="./EventTracker.png" class="card-img-top" alt="Project 3" style="height: 200px; object-fit: cover;">
                        <div class="card-body">
                            <h5 class="card-title"><span style="background: linear-gradient(45deg, #4499cc, #66cc99); -webkit-background-clip: text; background-clip: text; -webkit-text-fill-color: transparent;">Event</span>Tracker</h5>
                            <p class="card-text">This website allows you to store event information and track your favorite concerts, festivals, and other activities. It includes features like reminders and edition of already stored events</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="py-5">
        <div class="container">
            <h2 class="text-center mb-4">Skills</h2>
            <div class="row">
                <div class="col-md-6 text-center">
                    <h3 class="mt-2"><span style="color: #8A2BE2">Kotlin</span></h4>
                    <div class="progress mb-4 mt-4">
                        <div class="progress-bar Kotlin" role="progressbar" style="width: 90%">90%</div>
                    </div>
                    <h3 class="mt-4"><span style="color: #50C878">Compose</span></h4>
                    <div class="progress mb-3 mt-4">
                        <div class="progress-bar Compose" role="progressbar" style="width: 85%">85%</div>
                    </div>
                </div>
                <div class="col-md-6 text-center">
                    <h3 class="mt-2"><span style="color: #FFD700">JavaScript</span></h4>
                    <div class="progress mb-4 mt-4">
                        <div class="progress-bar Javascript" role="progressbar" style="width: 80%">95%</div>
                    </div>
                    <h3 class="mt-4"><span style="color: #4169E1">React</span></h4>
                    <div class="progress mb-3 mt-4">
                        <div class="progress-bar React" role="progressbar" style="width: 95%">80%</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Form -->
    <section id="contact" class="py-5 bg-light">
        <div class="container">
            <h2 class="text-center mb-4">Contact Me</h2>
            <div class="row justify-content-center">
                <div class="col-md-6">
                    <form>
                        <div class="mb-3">
                            <input type="text" class="form-control" placeholder="Your Name" required>
                        </div>
                        <div class="mb-3">
                            <input type="email" class="form-control" placeholder="Your Email" required>
                        </div>
                        <div class="mb-3">
                            <textarea class="form-control" rows="5" placeholder="Your Message" required></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-dark text-white text-center py-3">
        <p>&copy; 2025 <span style="background: linear-gradient(45deg, #66ccff, #99ccff, #ccffff); -webkit-background-clip: text; background-clip: text; -webkit-text-fill-color: transparent;">Dario's</span> Portfolio. All rights reserved.</p>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        // Sticky navbar
        let lastScroll = 0;
        window.addEventListener('scroll', () => {
            const currentScroll = window.pageYOffset;
            const navbar = document.getElementById('mainNav');
            
            if (currentScroll <= 0) {
                navbar.classList.remove('hidden');
                return;
            }
            
            if (currentScroll > lastScroll) {
                navbar.classList.add('hidden');
            } else {
                navbar.classList.remove('hidden');
            }
            lastScroll = currentScroll;
        });

        // Move card to middle
        function moveToMiddle(clickedIndex) {
            const cards = document.querySelectorAll('.project-card');
            cards.forEach(card => card.classList.remove('middle-card'));
            cards[clickedIndex].classList.add('middle-card');
        }
    </script>
</body>
</html></div>
```
