<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Roboto+Slab:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            background-color: white;
            font-family: 'Roboto Slab', serif;
            margin: 0; /* Remove default body margin */
        }
        .banner-image {
            width: 100%;
            max-height: 300px;
            object-fit: cover;
            display: block;
        }
        a {
            font-size: 1.2rem;
            color: black !important;
            text-decoration: none;
            text-transform: uppercase;
            cursor: pointer;
            padding: 5px 10px;
        }
        a:hover {
            text-decoration: underline;
        }
        #content {
            padding: 0; /* Ensure no extra padding around the content */
            margin: 0; /* Remove extra margin */
        }
        .ratio {
            margin-top: 1rem;
            margin-bottom: 1rem;
            background-color: black;
        }
        .top-buttons {
            display: flex;
            gap: 1.5rem;
            font-weight: bold;
            overflow-x: auto; /* Enable horizontal scrolling */
            white-space: nowrap; /* Prevent wrapping */
            padding: 10px 0; /* Add padding for better touch interaction */
            margin: 0; /* Remove default margin */
        }
        .top-buttons::-webkit-scrollbar {
            height: 8px; /* Adjust scrollbar height */
        }
        .top-buttons::-webkit-scrollbar-thumb {
            background-color: gray; /* Customize scrollbar thumb color */
            border-radius: 4px;
        }
        .top-buttons::-webkit-scrollbar-track {
            background-color: black; /* Customize scrollbar track color */
        }
        .video-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 1rem;
            justify-content: center;
            margin-top: 1rem;
        }
        footer {
            font-size: 0.7rem;
            opacity: 0.6;
        }
        @media (max-width: 768px) {
            h1 {
                font-size: 1.5rem;
            }
            a {
                font-size: 0.9rem;
            }
            .top-buttons {
                flex-wrap: nowrap;
                gap: 0.5rem;
            }
            .video-grid {
                grid-template-columns: 1fr;
            }
        }
        .image-display {
            margin-top: 1rem;
        }
        .image-display img {
            max-width: 100%;
            height: auto;
        }
        .text-display {
            margin-top: 1rem;
            font-size: 1.2rem;
            color: white;
        }
        .clickable-text {
            margin: 0 10px; /* Adds horizontal spacing between links */
            display: inline-block; /* Ensures margins apply consistently */
        }
        .selected {
            color: black !important;
            text-decoration: black underline;
        }
        .scrollable-container {
            display: flex;
            overflow-x: auto;
            white-space: nowrap;
            gap: 10px;
            padding: 10px 0;
        }
        .scrollable-container::-webkit-scrollbar {
            height: 8px;
        }
        .scrollable-container::-webkit-scrollbar-thumb {
            background-color: gray;
            border-radius: 4px;
        }
        .scrollable-container::-webkit-scrollbar-track {
            background-color: black;
        }
    </style>
</head>
<body>
    <!-- Banner Image -->
    <img src="https://pbs.twimg.com/media/GjXYL4PbkAAZeoR?format=jpg&name=4096x4096" alt="HAECHANSTRM Banner" class="banner-image">

    <!-- Top Links -->
    <div class="top-buttons">
        <a onclick="navigateTo('home')">HAECHAN</a>
        <a onclick="navigateTo('streaming-guidelines')">스트리밍 가이드라인</a>
        <a onclick="navigateTo('id-creation')">아이디 생성</a>
        <a onclick="navigateTo('playlist')">권장 스밍 리스트</a>
    </div>

    <!-- Content Section -->
    <div id="content">
        <section id="home" class="text-white text-center py-5">
            <div class="container">
                <div class="ratio ratio-16x9" style="max-width: 640px; margin: 0 auto;">
                    <iframe src="https://www.youtube.com/embed/0yzxJz-hHcc" title="YouTube video" allowfullscreen></iframe>
                </div>
                <div class="video-grid">
                    <div class="ratio ratio-16x9">
                        <iframe src="https://www.youtube.com/embed/MMJ_uIw02U8" title="YouTube video" allowfullscreen></iframe>
                    </div>
                    <div class="ratio ratio-16x9">
                        <iframe src="https://www.youtube.com/embed/AmtizylOpeA" title="YouTube video" allowfullscreen></iframe>
                    </div>
                </div>
            </div>
        </section>
    </div>

    <!-- Footer -->
    <footer class="bg-dark text-white text-center py-3">
        <p class="mb-0">&copy; 2025 HAECHANSTRM. All Rights Reserved.</p>
    </footer>

    <!-- JavaScript -->
    <script>
        const pages = {
            'home': `
                <section id="home" class="text-white text-center py-5">
                    <div class="container">
                        <div class="ratio ratio-16x9" style="max-width: 640px; margin: 0 auto;">
                            <iframe src="https://www.youtube.com/embed/0yzxJz-hHcc" title="YouTube video" allowfullscreen></iframe>
                        </div>
                        <div class="video-grid">
                            <div class="ratio ratio-16x9">
                                <iframe src="https://www.youtube.com/embed/MMJ_uIw02U8" title="YouTube video" allowfullscreen></iframe>
                            </div>
                            <div class="ratio ratio-16x9">
                                <iframe src="https://www.youtube.com/embed/AmtizylOpeA" title="YouTube video" allowfullscreen></iframe>
                            </div>
                        </div>
                    </div>
                </section>
            `,
            'streaming-guidelines': `
                <section class="text-white text-center py-5">
                    <div class="container">
                        <div class="scrollable-container">
                            <a class="clickable-text" onclick="showImage('youtube', 'streaming-guidelines')">YouTube M/V</a>
                            <a class="clickable-text" onclick="showImage('melon', 'streaming-guidelines')">Melon</a>
                            <a class="clickable-text" onclick="showImage('genie', 'streaming-guidelines')">Genie</a>
                            <a class="clickable-text" onclick="showImage('bugs', 'streaming-guidelines')">Bugs</a>
                            <a class="clickable-text" onclick="showImage('flo', 'streaming-guidelines')">Flo</a>
                            <a class="clickable-text" onclick="showImage('kakao', 'streaming-guidelines')">Kakao Music</a>
                        </div>
                        <div class="image-display" id="image-display"></div>
                    </div>
                </section>
            `,
            'id-creation': `
                <section class="text-white text-center py-5">
                    <div class="container">
                        <div class="scrollable-container">
                            <a class="clickable-text" onclick="showImage('melon', 'id-creation')">Melon</a>
                            <a class="clickable-text" onclick="showImage('genie', 'id-creation')">Genie</a>
                            <a class="clickable-text" onclick="showImage('bugs', 'id-creation')">Bugs</a>
                            <a class="clickable-text" onclick="showImage('flo', 'id-creation')">Flo</a>
                            <a class="clickable-text" onclick="showImage('kakao', 'id-creation')">Kakao Music</a>
                        </div>
                        <div class="image-display" id="image-display"></div>
                    </div>
                </section>
            `,
            'playlist': `
                <section class="text-white text-center py-5">
                    <div class="container">
                        <div class="scrollable-container">
                            <a class="clickable-text" onclick="showText('haechan-solo')">HAECHAN 1st Solo Album</a>
                        </div>
                        <div class="text-display" id="text-display"></div>
                    </div>
                </section>
            `
        };

        function navigateTo(page) {
            const contentDiv = document.getElementById('content');
            contentDiv.innerHTML = pages[page];
        }
        function showImage(platform, section) {
            const images = {
                'streaming-guidelines': {
                    'youtube': 'https://pbs.twimg.com/media/GjW1lSaaYAA55nN?format=jpg&name=4096x4096',
                    'melon': 'https://via.placeholder.com/300?text=Melon+Streaming',
                    'genie': 'https://via.placeholder.com/300?text=Genie+Streaming',
                    'bugs': 'https://via.placeholder.com/300?text=Bugs+Streaming',
                    'flo': 'https://via.placeholder.com/300?text=Flo+Streaming',
                    'kakao': 'https://via.placeholder.com/300?text=Kakao+Music+Streaming'
                },
                'id-creation': {
                    'melon': 'https://via.placeholder.com/300?text=Melon+ID+Creation',
                    'genie': 'https://via.placeholder.com/300?text=Genie+ID+Creation',
                    'bugs': 'https://via.placeholder.com/300?text=Bugs+ID+Creation',
                    'flo': 'https://via.placeholder.com/300?text=Flo+ID+Creation',
                    'kakao': 'https://via.placeholder.com/300?text=Kakao+Music+ID+Creation'
                }
            };
            const imageDisplay = document.getElementById('image-display');
            imageDisplay.innerHTML = `<img src="${images[section][platform]}" alt="${platform} ${section}">`;
        }
        function showText(content) {
            const texts = {
                'haechan-solo': 'Here is the recommended playlist for HAECHAN\'s 1st Solo Album...'
            };
            const textDisplay = document.getElementById('text-display');
            textDisplay.innerHTML = texts[content];
        }
    </script>
</body>
</html>
