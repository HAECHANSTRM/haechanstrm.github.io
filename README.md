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
            color: white !important; /* Force white font color */
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
                        <p>Melon, Genie, Bugs, Flo, Kakao Music.</p>
                    </div>
                </section>
            `,
            'id-creation': `
                <section class="text-white text-center py-5">
                    <div class="container">
                        <h1>아이디 생성</h1>
                        <p>Melon, Genie, Bugs, Flo, Kakao Music.</p>
                    </div>
                </section>
            `,
            'playlist': `
                <section class="text-white text-center py-5">
                    <div class="container">
                        <h1>플레이리스트</h1>
                        <p>Good Person, Haechan 1st Solo Album.</p>
                    </div>
                </section>
            `
        };

        function navigateTo(page) {
            const contentDiv = document.getElementById('content');
            contentDiv.innerHTML = pages[page];
        }
    </script>
</body>
</html>
