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
        .btn {
            font-size: 1rem;
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
            justify-content: flex-end;
            gap: 1rem;
            margin-bottom: 1rem;
        }
        @media (max-width: 768px) {
            h1 {
                font-size: 1.5rem;
            }
            .btn {
                font-size: 0.9rem;
                padding: 0.5rem 0.8rem;
            }
            .navbar-brand {
                font-size: 1.2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Hero Section -->
    <section id="home" class="bg-dark text-white text-center py-5">
        <div class="container">
            <div class="top-buttons">
                <a href="#streaming-guideline" class="btn btn-light btn-lg">Streaming Guideline</a>
                <a href="#id-creation" class="btn btn-light btn-lg">ID Creation</a>
                <a href="#playlist" class="btn btn-light btn-lg">Playlist</a>
            </div>
            <div class="ratio ratio-4x3" style="max-width: 480px; margin: 0 auto;">
                <iframe src="https://www.youtube.com/embed/0yzxJz-hHcc" title="YouTube video" allowfullscreen></iframe>
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
