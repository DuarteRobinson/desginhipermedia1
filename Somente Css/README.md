<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ficha15</title>
</head>

<body>
    <button class="botao" id="anim1">1</button>
    <button class="botao" id="anim2">2</button>
    <button class="botao" id="anim3">3</button>
    <button class="botao" id="anim4">4</button>
    <button class="botao" id="anim5">5</button>
    <button class="botao" id="anim6">6</button>

    <style>
        .botao {
            width: 150px;
            height: 80px;
            margin: 20px;
            background-color: transparent;
            border: none;
            color: blueviolet;
            cursor: pointer;
        }
        #anim1 {
            border: 3px solid blueviolet;
            transition-duration: 200ms;
        }
        #anim1:hover {
            background-color: blueviolet;
            color: white;
        }
        #anim2 {
            position: relative;
        }
        #anim2::before {
            position: absolute;
            content: '';
            top: 0;
            left: 0;
            width: 0;
            height: 3px;
            background-color: violet;

            transition-duration: 200ms;
        }
        #anim2::after {
            position:absolute;
            content: '';
            bottom: 0;
            right: 0;
            width: 0;
            height: 3px;
            background-color: violet;
            transition-duration: 200ms;
        }
        #anim2:hover::before,
        #anim2:hover::after {
            width: 100%;
        }
        #anim3{
            position: relative;
            transition-duration: 200ms;
        }
        #anim3::after{
            position: absolute;
            content: '';
            bottom: 0;
            left: 0;
            width: 100%;
            height: 0;
            background-color: blue;
            z-index: -1;

            transition-duration: 200ms;
        }
        #anim3:hover{
            color: white;
        }
        #anim3:hover::after{
            height: 100%;
        }
        #anim4{
            position: relative;
            transition-duration: 200ms;
        }
        #anim4::before{
            position: absolute;
            content: '';
            top: 0;
            left: 0;
            width: 0;
            height: 0;
            background-color: aqua;
            z-index: -1;
            transition: 200ms;
        }
        #anim4::after{
            position: absolute;
            content: '';
            bottom: 0;
            right: 0;
            width: 0;
            height: 0;
            background-color: aqua;
            z-index: -1;
            transition: 200ms;
        }
        #anim4:hover{
            color: white;
        }
        #anim4:hover::before
        #anim4:hover::after
    </style>

</body>

</html>