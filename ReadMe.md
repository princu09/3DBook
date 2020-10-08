## 3D Book CSS Layout Free Source Code By NorthFox Developers

##### 📫 Connect with me here:<br />
 <br />
 <p>
  <a target="_blank" href="https://www.instagram.com/princu.09">
    <img src="https://img.shields.io/badge/princu.09-386938188?style=flat&logo=instagram&color=black">
  </a> &nbsp; 
  <a target="_blank" href="https://twitter.com/princu09">
    <img src="https://img.shields.io/badge/@princu09-30302f?style=flat&logo=twitter&color=black">
  </a>&nbsp; 
  <a target="_blank" href="https://github.com/princu09">
    <img src="https://img.shields.io/badge/@princu09-30302f?style=flat&logo=github&color=black">
  </a>&nbsp;
    <a target="_blank" href="https://www.t.me/proghub09">
    <img src="https://img.shields.io/badge/ProgHub09-386938188?style=flat&logo=telegram&color=black">
  </a>
</p>


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
