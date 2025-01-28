<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine's Request</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-family: 'Comic Sans MS', 'Comic Sans', cursive;
            background-color: white;
            text-align: center;
        }
        .container {
            padding: 20px;
            border-radius: 10px;
        }
        h1 {
            margin-bottom: 20px;
        }
        .button {
            font-size: 18px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .yes-button {
            background-color: #28a745;
            color: white;
            transition: font-size 0.2s ease;
        }
        .no-button {
            background-color: #dc3545;
            color: white;
        }
        .hidden {
            display: none;
        }
        .gif {
            width: 100%;
            max-width: 500px;
            margin-bottom: 20px;
        }
    </style>
    <script type="text/javascript" async src="https://tenor.com/embed.js"></script>
</head>
<body>
    <div class="container">
        <div class="tenor-gif-embed" data-postid="6089043773656829204" data-share-method="host" data-aspect-ratio="1.23333" data-width="100%">
            <a href="https://tenor.com/view/jumping-bear-hearts-no-png-gif-6089043773656829204">Jumping Bear Hearts No Png Sticker</a>
            from <a href="https://tenor.com/search/jumping+bear+hearts+no+png-stickers">Jumping Bear Hearts No Png Stickers</a>
        </div>
        <h1>Will you be my Valentine?</h1>
        <button class="button yes-button" id="yes-button">Yes</button>
        <button class="button no-button" id="no-button">No</button>
        <p id="message"></p>
    </div>

    <script>
        const yesButton = document.getElementById('yes-button');
        const noButton = document.getElementById('no-button');
        const message = document.getElementById('message');
        const container = document.querySelector('.container');

        let noClickCount = 0;
        const noMessages = [
            "Are you sure?",
            "Really sure?",
            "Just think about it...",
            "You're breaking my heart...",
            "I'll be very sad...",
            "Why not give it a try?",
            "You know you want to say yes...",
            "Please reconsider...",
            "It would mean so much...",
            "Don't make me cry!"
        ];

        yesButton.addEventListener('click', () => {
            container.innerHTML = `
                <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExOXg0N3lwYnpxcmRnengxZWU0dGozenljdDdnczc1aDRpN2plNzd2cyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/IzXiddo2twMmdmU8Lv/giphy.gif" alt="Two bears hugging" class="gif">
                <h1>Ok yay!!!</h1>
            `;
        });

        noButton.addEventListener('click', () => {
            if (noClickCount < noMessages.length) {
                noButton.textContent = noMessages[noClickCount];
                noClickCount++;
            }
            yesButton.style.fontSize = parseInt(window.getComputedStyle(yesButton).fontSize) + 20 + 'px';
        });
    </script>
</body>
</html>
