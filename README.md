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
            color: white;
            text-decoration: none;
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
        }
        .top-buttons {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-bottom: 1rem;
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
                font-size: 1rem;
            }
            .video-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <section id="home" class="bg-dark text-white text-center py-5">
        <div class="container">
            <div class="top-buttons">
                <a href="#streaming-guideline">Streaming Guideline</a>
                <a href="#id-creation">ID Creation</a>
                <a href="#playlist">Playlist</a>
            </div>
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

    <!-- Footer -->
    <footer class="bg-dark text-white text-center py-3">
        <p class="mb-0">&copy; 2025 HAECHANSTRM. All Rights Reserved.</p>
    </footer>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
