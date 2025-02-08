<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HAECHANSTRM</title>
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/css/bootstrap.min.css" rel="stylesheet">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Roboto+Slab:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            background-color: black;
            font-family: 'Roboto Slab', serif;
        }
        a {
            font-size: 1.2rem;
            color: white !important;
            text-decoration: none;
            text-transform: uppercase;
            cursor: pointer;
        }
        a:hover {
            text-decoration: underline;
        }
        #home {
            padding-top: 3rem;
            padding-bottom: 3rem;
        }
        .ratio {
            margin-top: 1rem;
            margin-bottom: 1rem;
            background-color: black;
        }
        .top-buttons {
            display: flex;
            justify-content: flex-start;
            gap: 1.5rem;
            margin-bottom: 1rem;
            font-weight: bold;
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
                flex-wrap: wrap;
                gap: 0.5rem;
            }
            .video-grid {
                grid-template-columns: 1fr;
            }
        }
        .image-display {
            margin-top: 2rem;
        }
        .image-display img {
            max-width: 100%;
            height: auto;
        }
        .text-display {
            margin-top: 2rem;
            font-size: 1.2rem;
            color: white;
        }
    </style>
</head>
<body>
    <!-- Top Links -->
    <div class="top-buttons">
        <a onclick="navigateTo('home')">HAECHAN</a>
        <a onclick="navigateTo('streaming-guidelines')">스트리밍 가이드라인</a>
        <a onclick="navigateTo('id-creation')">아이디 생성</a>
        <a onclick="navigateTo('playlist')">플레이리스트</a>
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
                        <h1>스트리밍 가이드라인</h1>
                        <p>
                            <a onclick="showImage('melon', 'streaming-guidelines')">Melon</a>, 
                            <a onclick="showImage('genie', 'streaming-guidelines')">Genie</a>, 
                            <a onclick="showImage('bugs', 'streaming-guidelines')">Bugs</a>, 
                            <a onclick="showImage('flo', 'streaming-guidelines')">Flo</a>, 
                            <a onclick="showImage('kakao', 'streaming-guidelines')">Kakao Music</a>.
                        </p>
                        <div class="image-display" id="image-display"></div>
                    </div>
                </section>
            `,
            'id-creation': `
                <section class="text-white text-center py-5">
                    <div class="container">
                        <h1>아이디 생성</h1>
                        <p>
                            <a onclick="showImage('melon', 'id-creation')">Melon</a>, 
                            <a onclick="showImage('genie', 'id-creation')">Genie</a>, 
                            <a onclick="showImage('bugs', 'id-creation')">Bugs</a>, 
                            <a onclick="showImage('flo', 'id-creation')">Flo</a>, 
                            <a onclick="showImage('kakao', 'id-creation')">Kakao Music</a>.
                        </p>
                        <div class="image-display" id="image-display"></div>
                    </div>
                </section>
            `,
            'playlist': `
                <section class="text-white text-center py-5">
                    <div class="container">
                        <h1>플레이리스트</h1>
                        <p>
                            <a onclick="showText('good-person')">Good Person</a>, 
                            <a onclick="showText('haechan-solo')">Haechan 1st Solo Album</a>.
                        </p>
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
                    'kakao': 'https://via.placeholder.com/300?text=Kakao+ID+Creation'
                }
            };

            const imageDisplay = document.getElementById('image-display');
            imageDisplay.innerHTML = `<img src="${images[section][platform]}" alt="${platform} image">`;
        }

        function showText(option) {
            const texts = {
                'good-person': 'Haechan First OST Clickable Playlists.',
                'haechan-solo': 'Haechan 1st Solo Album Clickable Playlists'
            };

            const textDisplay = document.getElementById('text-display');
            textDisplay.innerHTML = `<p>${texts[option]}</p>`;
        }
    </script>
</body>
</html>
