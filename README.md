<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <title>浩鋒的影片魔法網頁</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding-top: 50px;
            transition: background-color 0.5s;
            overflow: hidden;
        }
        button {
            font-size: 1.5em;
            padding: 15px 30px;
            cursor: pointer;
            border: none;
            border-radius: 10px;
            background-color: #4CAF50;
            color: white;
            margin-bottom: 20px;
        }
        #magicVideo {
            display: none;
            width: 60%;
            border: 5px solid #fff;
            border-radius: 15px;
            box-shadow: 0 0 20px rgba(0,0,0,0.5);
        }
    </style>
</head>
<body>
<button id="magicBtn">點我釋放影片魔法！</button>
<p id="message"></p>
<video id="magicVideo" controls>
    <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4">
    你的瀏覽器不支援影片播放
</video>

<script>
    const button = document.getElementById('magicBtn');
    const message = document.getElementById('message');
    const video = document.getElementById('magicVideo');

    button.addEventListener('click', () => {
        // 背景隨機顏色
        const r = Math.floor(Math.random()*256);
        const g = Math.floor(Math.random()*256);
        const b = Math.floor(Math.random()*256);
        document.body.style.backgroundColor = `rgb(${r},${g},${b})`;

        // 隨機訊息
        const messages = ["浩鋒，你今天真帥！","程式天才浩鋒在此！","魔法啟動！"];
        message.textContent = messages[Math.floor(Math.random()*messages.length)];

        // 顯示並播放影片
        video.style.display = 'block';
        video.currentTime = 0;
        video.play();
    });
</script>
</body>
</html>
