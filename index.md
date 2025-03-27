---
layout: post
title: Flocker Social Media Site 
search_exclude: true
description: Login and explore our social media hub for everything DNHS 
hide: true
menu: nav/home.html
---




<head>
    <title>Nighthawk Tok</title>
    <link rel="stylesheet" href="styles.css">
    <script defer src="script.js"></script>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(to right, #001f3f, #007f5f);
            color: white;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        header {
            background: rgba(0, 31, 63, 0.9);
            padding: 20px;
            width: 100%;
            text-align: center;
        }
        nav ul {
            list-style: none;
            padding: 0;
        }
        nav ul li {
            display: inline;
            margin: 0 15px;
        }
        nav a {
            color: white;
            text-decoration: none;
            font-size: 18px;
        }
        main {
            display: flex;
            justify-content: space-between;
            width: 90%;
            max-width: 1200px;
            padding: 20px;
        }
        aside {
            width: 20%;
            background: rgba(0, 31, 63, 0.8);
            padding: 15px;
            border-radius: 10px;
        }
        .feed-container {
            width: 55%;
        }
        .post {
            background: rgba(255, 255, 255, 0.2);
            padding: 15px;
            margin: 15px 0;
            border-radius: 10px;
            text-align: left;
        }
        .like-btn {
            background: #007f5f;
            border: none;
            color: white;
            padding: 5px 10px;
            border-radius: 5px;
            cursor: pointer;
        }
        .like-btn:hover {
            background: #005f47;
        }
        footer {
            margin-top: 20px;
            background: rgba(0, 31, 63, 0.9);
            padding: 10px;
            width: 100%;
            text-align: center;
        }
        
        .timeline-container {
            width: 90%;
            max-width: 1200px;
            margin-top: 50px;
            text-align: center;
        }
        .timeline {
            display: flex;
            justify-content: center;
            gap: 15px;
        }
        .year {
            padding: 10px 15px;
            background: #007f5f;
            border-radius: 5px;
            cursor: pointer;
            transition: 0.3s;
        }
        .year:hover, .year.active {
            background: #005f47;
        }
        .student-list {
            margin-top: 20px;
            background: rgba(255, 255, 255, 0.2);
            padding: 15px;
            border-radius: 10px;
            display: none;
        }
        /* Chatbox styles */
        .chatbox-container {
            width: 100%;
            max-width: 500px;
            background: rgba(0, 31, 63, 0.8);
            border-radius: 10px;
            padding: 15px;
            position: fixed;  /* Fixed position to stay at the bottom */
            bottom: 20px;     /* Distance from the bottom of the viewport */
            left: 50%;
            transform: translateX(-50%); /* Center it horizontally */
            z-index: 999; /* Ensure it's on top of other content */
        }

        .chatbox-header {
            text-align: center;
            color: white;
        }

        .chatbox-messages {
            height: 200px;
            overflow-y: auto;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 5px;
            margin-bottom: 10px;
            padding: 10px;
        }

        .chatbox-input {
            display: flex;
            justify-content: space-between;
        }

        .chatbox-input input {
            width: 80%;
            padding: 10px;
            border-radius: 5px;
            border: none;
        }

        .chatbox-input button {
            background: #007f5f;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .chatbox-input button:hover {
            background: #005f47;
        }

        .chat-message {
            background: #fff;
            color: black;
            padding: 8px;
            margin: 5px 0;
            border-radius: 5px;
            max-width: 80%;
        }

        .chat-message.me {
            background: #007f5f;
            color: white;
            margin-left: auto;
        }

    </style>
</head>
<body>
    <header>
        <h1>Welcome to Nighthawk Tok</h1>
        <nav>
            <ul>
                <li><a href="#feed">Feed</a></li>
                <li><a href="#explore">Explore</a></li>
                <li><a href="#profile">Profile</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <aside>
            <h3>Trending</h3>
            <p>#GoNighthawks</p>
            <p>#CodingLife</p>
            <p>#NighthawkPride</p>
        </aside>
        
        <div class="feed-container">
            <section id="feed">
                <h2>Latest Posts</h2>
                <div class="post">
                    <h3>@student1</h3>
                    <p>Had a great time at the football game! #GoNighthawks</p>
                    <button class="like-btn" onclick="likePost(this)">❤️ Like</button>
                    <span class="like-count">0</span>
                </div>
                <div class="post">
                    <h3>@student2</h3>
                    <p>Check out my latest project for coding class! 🚀</p>
                    <button class="like-btn" onclick="likePost(this)">❤️ Like</button>
                    <span class="like-count">0</span>
                </div>
            </section>
        </div>
        
        <aside>
            <h3>Suggested Friends</h3>
            <p>@nighthawk2025</p>
            <p>@codingwizard</p>
            <p>@sportsfan99</p>
        </aside>
    </main>
    
    <div class="timeline-container">
        <h2>Student Timeline</h2>
        <div class="timeline">
            <span class="year" onclick="showStudents(2018)">2018</span>
            <span class="year" onclick="showStudents(2019)">2019</span>
            <span class="year" onclick="showStudents(2020)">2020</span>
            <span class="year" onclick="showStudents(2021)">2021</span>
            <span class="year" onclick="showStudents(2022)">2022</span>
            <span class="year" onclick="showStudents(2023)">2023</span>
            <span class="year" onclick="showStudents(2024)">2024</span>
            <span class="year" onclick="showStudents(2025)">2025</span>
        </div>
        <div id="students" class="student-list"></div>
    </div>
    
    <footer>
        <p>&copy; 2025 Nighthawk Tok. Created by Del Norte Students.</p>
            <div class="chatbox-container">
    </div>
    </footer>

        <div class="chatbox-header">
            <h3>Chat</h3>
        </div>
        <div class="chatbox-messages" id="chatboxMessages">
            <!-- Chat messages will be displayed here -->
        </div>
        <div class="chatbox-input">
            <input type="text" id="chatInput" placeholder="Type a message..." />
            <button onclick="sendMessage()">Send</button>
        </div>
    
    <script>
        const studentData = {
            2018: ['Alice Johnson', 'Bob Smith', 'Charlie Lee'],
            2019: ['David Green', 'Emma Brown', 'Frank White'],
            2020: ['Grace Adams', 'Henry Clark', 'Ivy Martinez'],
            2021: ['Jack Wilson', 'Kelly Rogers', 'Leo Turner'],
            2022: ['Mia Scott', 'Noah Edwards', 'Olivia Harris'],
            2023: ['Paul King', 'Quinn Baker', 'Rachel Adams'],
            2024: ['Sam Foster', 'Tina Brooks', 'Ulysses Carter'],
            2025: ['Victor Davis', 'Wendy Hall', 'Xander Lopez']
        };
        function showStudents(year) {
            const studentList = document.getElementById('students');
            studentList.innerHTML = `<h3>Students from ${year}</h3><p>${studentData[year].join(', ')}</p>`;
            studentList.style.display = 'block';
        }
            // Function to send a message
    function sendMessage() {
        const chatInput = document.getElementById('chatInput');
        const message = chatInput.value.trim();
        
        if (message) {
            // Create a new message element
            const newMessage = document.createElement('div');
            newMessage.classList.add('chat-message', 'me');
            newMessage.innerText = message;

            // Append the new message to the chatbox messages container
            const chatboxMessages = document.getElementById('chatboxMessages');
            chatboxMessages.appendChild(newMessage);
            
            // Scroll to the bottom
            chatboxMessages.scrollTop = chatboxMessages.scrollHeight;

            // Clear the input field
            chatInput.value = '';
        }
    }

    </script>

</body>
