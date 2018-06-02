<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        .boxout {
            width: 500px;
            height: 500px;
            border: 1px solid red;
            margin: 50px;
            position: relative;
            perspective: 800px;
            background-color: rgba(236, 16, 16, 0.2)
        }

        .boxin {
            width: 400px;
            height: 400px;
            border: 1px solid blue;
            border-radius: 5%;
            position: absolute;
            top: 50px;
            left: 50px;
            transform-style: preserve-3d;
            /* perspective: 400px; */
            /* transition: all 4s; */
            animation: circle 4s linear infinite;
        }

        /* .boxin:hover {

            transform: rotateX(720deg);
        } */

        @keyframes circle {
            from {
                transform: rotateX(0deg) rotateY(0deg) rotateZ(0deg);
                /* transform: rotateY(0deg); */
            }
            to {
                transform: rotateX(360deg) rotateY(360deg) rotateZ(360deg);
                /* transform: rotateY(360deg); */
            }
        }

        .boxin:hover {
            animation-play-state: paused;
        }

        .top {
            width: 200px;
            height: 200px;
            background-color: rgba(255, 0, 0, 0.6);
            position: absolute;
            top: 0;
            left: 100px;
            text-align: center;
            line-height: 200px;
            color: white;
            font-size: 30px;
            transform: rotateX(90deg);
            border-radius: 5%;
        }

        .bottom {
            width: 200px;
            height: 200px;
            background-color: rgba(0, 255, 0, 0.6);
            position: absolute;
            bottom: 0;
            left: 100px;
            text-align: center;
            line-height: 200px;
            color: white;
            font-size: 30px;
            transform: rotateX(90deg);
            border-radius: 5%;
        }

        .left {

            width: 200px;
            height: 200px;
            background-color: rgba(0, 0, 255, 0.6);
            position: absolute;
            bottom: 100px;
            left: 0px;
            text-align: center;
            line-height: 200px;
            color: white;
            font-size: 30px;
            transform: rotateY(90deg);
            border-radius: 5%;
        }


        .right {
            width: 200px;
            height: 200px;
            background-color: rgba(116, 13, 235, 0.6);
            position: absolute;
            bottom: 100px;
            right: 0px;
            text-align: center;
            line-height: 200px;
            color: white;
            font-size: 30px;
            transform: rotateY(90deg);
            border-radius: 5%;
        }

        .in {
            width: 200px;
            height: 200px;
            background-color: rgba(0, 0, 0, 0.6);
            position: absolute;
            transform: translateZ(100px);
            top: 100px;
            left: 100px;
            text-align: center;
            line-height: 200px;
            color: white;
            font-size: 30px;
            border-radius: 5%;
        }

        .out {
            width: 200px;
            height: 200px;
            background-color: rgba(255, 255, 255, 0.6);
            position: absolute;
            transform: translateZ(-100px);
            top: 100px;
            left: 100px;
            text-align: center;
            line-height: 200px;
            color: red;
            font-size: 30px;
            border-radius: 5%;
        }
    </style>
</head>

<body>
    <div class="boxout">
        <div class="boxin">
            <div class="top">上</div>
            <div class="bottom">下</div>
            <div class="in">前</div>
            <div class="out">后</div>
            <div class="left">左</div>
            <div class="right">右</div>
        </div>

    </div>
</body>

</html>
