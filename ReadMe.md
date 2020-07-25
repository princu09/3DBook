## 3D Book CSS Layout Free Source Code By NorthFox Developers

#### Join Our Telegram Channel [ProgHub09](http://t.me/ProgHub09) and Also Download Our App.

![Video Here](images/3DBook.gif)


#### HTML File

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>3D Book</title>
    <link rel="stylesheet" href="style.css">
    <link rel="shortcut icon" href="https://princu09.github.io/nfwebbuilder/img/logo.png" type="image/png">
</head>

<body>
    <section>
        <div class="book">
            <img src="images/Front.jpg" alt="Book Image">
        </div>
    </section>
</body>

</html>
```

#### CSS File

```
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: url(images/BG.jpeg);
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: fixed;
}

section {
    display: flex;
    justify-content: center;
    align-items: center;
    transform-style: preserve-3d;
    perspective: 1000px;
}

section .book {
    position: relative;
    width: 383px;
    height: 567px;
    box-shadow: 20px 20px 20px rgba(0, 0, 0, 0.2);
    transform-style: preserve-3d;
    transition: 0.5s;
}

section .book:hover {
    transform: rotateY(35deg);
    box-shadow: 0px 20px 20px rgba(0, 0, 0, 0.2);
}

section .book:active {
    transform: rotateY(180deg);
}

section .book:before {
    content: '';
    position: absolute;
    width: 60px;
    height: 100%;
    transform-origin: left;
    background: url(http://source.unsplash.com/random);
    background-size: cover;
    background-position: center;
    transform: rotateY(90deg);
}

section .book:after {
    content: '';
    position: absolute;
    width: 100%;
    height: 100%;
    transform-origin: center;
    background: url(images/Back.jpg);
    background-position: center;
    transform: rotateY(180deg) translateZ(60px);
}

section .book img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
}

@media screen and (max-width:786px) {
    section .book {
        width: 300px;
        height: 460px;
    }
}
```