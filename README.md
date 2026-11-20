<!DOCTYPE html>
<html>
<head>
    <title>Image Gallery</title>
    <style>
        body {
            font-family: Arial;
            text-align: center;
            background: #f2f2f2;
        }
        h2 {
            color: darkblue;
        }
        #bigImage {
            width: 500px;
            height: 300px;
            object-fit: cover;
            border-radius: 10px;
            margin-top: 20px;
        }
        .gallery {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
        }
        .gallery img {
            width: 100px;
            height: 80px;
            object-fit: cover;
            border-radius: 8px;
            cursor: pointer;
        }
        .gallery img:hover {
            transform: scale(1.1);
            border: 3px solid blue;
        }
    </style>
</head>

<body>
    <h2>My Image Gallery</h2>

    <div>
        <img id="bigImage"
        src="https://picsum.photos/id/1015/500/300">
    </div>
    <div class="gallery" id="gallery"></div>
    <script>
        let images = [
            "https://picsum.photos/id/1015/500/300",
            "https://picsum.photos/id/1016/500/300",
            "https://picsum.photos/id/1025/500/300",
            "https://picsum.photos/id/1035/500/300",
            "https://picsum.photos/id/1043/500/300",
            "https://picsum.photos/id/106/500/300"
        ];
        let gallery = document.getElementById("gallery");
        let bigImage = document.getElementById("bigImage");
        for (let i = 0; i < images.length; i++) {
            let img = document.createElement("img");
            img.src = images[i];
            img.onclick = function() {
                bigImage.src = images[i];
            };
            gallery.appendChild(img);
        }

    </script>

</body>
</html>
