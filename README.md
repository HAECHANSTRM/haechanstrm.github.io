<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HAECHANSTRM</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }
        header {
            background-color: #333;
            color: white;
            padding: 10px 20px;
            display: flex;
            align-items: center;
        }
        .nav-buttons {
            display: flex;
            gap: 15px;
        }
        .nav-buttons a {
            color: white;
            text-decoration: none;
            font-weight: bold;
        }
        .nav-buttons a:hover {
            text-decoration: underline;
        }
        main {
            text-align: center;
            margin-top: 50px;
        }
        footer {
            margin-top: 50px;
            background-color: #333;
            color: white;
            text-align: center;
            padding: 10px 0;
            position: fixed;
            bottom: 0;
            width: 100%;
        }
    </style>
</head>
<body>
    <header>
        <nav class="nav-buttons">
            <a href="#home">Home</a>
            <a href="#streaming-guideline">Streaming Guideline</a>
            <a href="#id-creation">ID Creation</a>
            <a href="#playlist">Playlist</a>
        </nav>
    </header>
    <main id="home">
        <h1>Welcome to HAECHANSTRM</h1>
        <div>
            <iframe width="560" height="315" src="https://www.youtube.com/embed/0yzxJz-hHcc" 
                title="YouTube video player" frameborder="0" 
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen>
            </iframe>
        </div>
    </main>
    <footer>
        2025 HAECHANSTRM. All Rights Reserved.
    </footer>
</body>
</html>
