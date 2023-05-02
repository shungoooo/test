# test
<!DOCTYPE html>
<html>
<head>
    <title>キャラクター選択画面</title>
    <style>
        .character {
            width: 100px;
            height: 100px;
            margin: 10px;
        }

        .selected {
            border: 3px solid red;
        }
    </style>
</head>
<body>
    <div id="characters">
        <img src="character1.png" class="character" id="char1">
        <img src="character2.png" class="character" id="char2">
        <img src="character3.png" class="character" id="char3">
        <!-- キャラクターの画像を追加 -->
    </div>

    <script>
        var characters = document.getElementsByClassName('character');

        for (let i = 0; i < characters.length; i++) {
            characters[i].addEventListener('click', function() {
                for (let j = 0; j < characters.length; j++) {
                    characters[j].classList.remove('selected');
                }
                this.classList.add('selected');
            });
        }
    </script>
</body>
</html>
