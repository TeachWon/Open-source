<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, maximum-scale=1, user-scalable=no">
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <meta name="description" content="TeachWon's Blog">
    <meta name="author" content="TeachWon">
    <meta name="keywords" content="blog, TeachWon, web development">
    <title>TeachWon's Blog</title>
    <link rel="icon" href="https://cdn-icons-png.flaticon.com/128/2593/2593542.png" type="image/x-icon">
    <link rel="stylesheet" href="styles.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Dongle:wght@300&display=swap" rel="stylesheet">
</head>

<body>
    <header>
        <div class="header-shows">
            <div class="header-img" id="BlueLogo">
            </div>
            <div class="nav-menu nav-menu-center" style="pointer-events: none;">TeachWon's Blog</div>
        </div>
        <div class="nav-button">
            <nav>
                <ul class="nav-menu nav-menu-github">
                    <li>
                        <a href="https://github.com/TeachWon">
                            <i class="fab fa-github"></i> GitHub
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>

    <div id="portfolio" class="card-container">
        <div class="flex-container">
            <div class="left-column">
                <div class="flex-holder">
                    <div class="col text-col aos-init aos-animate" data-aos="fade-up">
                        <div class="content-holder">
                            <div class="title-holder">
                                <div class="top-image-holder">
                                    <img class="profile_pic" src="media/b_40909dc6e3fbd1932b3450786bb11bcc.jpg">
                                    <h1>TeachWon</h1>
                                </div>
                                <h1 class="profile_name" style="color: rgba(255, 255, 255, 0.75);">About me:</h1>
                            </div>
                            <div class="left-box-text-holder">
                                <p> I am TeachWon, male, 20 years old, a member of the Communist Party of China from Wuqing, Tianjin. 
                                    I am currently studying software engineering at the School of Computer Science, Hubei University, 
                                    Wuchang District, Wuhan City, Hubei Province, China. I like to play video games, especially League of Legends, 
                                    Horizon 5, Hearthstone Tavern Battle Chess. I have a keen interest in world history, especially Chinese history.
                                    Usually like to brush Tiktok, watching funny, basketball, video games and other plates. I'm a LeBron James fan. 
                                    I'm also a fan of Kang Seung-rok and Lee Sang-hyuk. In music, I am a melody lover and a fan of Wang Leehom.
                                </p>
                                <p>
                                    I am very happy to let you know me in the way of personal blog!
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div style="padding: 8px;"></div>

            <div class="right-column">
                <div class="col gallery-col">
                    <div class="col-inner-holder aos-init aos-animate" data-aos="fade-up" data-aos-delay="250">
                        <div class="text-holder">
                            <h1 class="profile_name" style="color: rgba(255, 255, 255, 0.75);">GitHub Project:</h1>
                            <div class="right-box-text-holder">
                                <p> 
                                    This personal blog is mainly used for my final examination report of open source course design this semester. 
                                    While completing my final examination, I hope to help more people understand open source projects and HTML web 
                                    design through GitHub, an open source platform.
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Section to display README content -->
    <div id="readme-content" class="readme-container">
        <h2>Project README</h2>
        <div id="readme-text" class="readme-text"></div>
    </div>

    <footer class="footer">
        <div class="inner-footer-contain">
            <p>&copy; 2024 TeachWon Copyright</p>
        </div>
    </footer>

    <script>
        // Fetch and display the README file from GitHub
        fetch('https://api.github.com/repos/TeachWon/YourRepository/contents/README.md')
            .then(response => response.json())
            .then(data => {
                // Decode the Base64 content of the README file
                const readmeContent = atob(data.content);
                document.getElementById('readme-text').innerHTML = marked(readmeContent);
            })
            .catch(error => console.error('Error fetching README.md:', error));

        // Use marked.js to parse and render the markdown content into HTML
        // You can include marked.js from a CDN or locally for markdown parsing
        const script = document.createElement('script');
        script.src = 'https://cdnjs.cloudflare.com/ajax/libs/marked/4.0.12/marked.min.js';
        document.head.appendChild(script);
    </script>
</body>
</html>
