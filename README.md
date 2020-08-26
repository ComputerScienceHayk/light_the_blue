# light_the_blue

![img alt](https://github.com/ComputerScienceHayk/light_the_blue/blob/master/screen.gif)

#html
```
...
<body class="body">
    <div class="moth">
        <div class="moth__body"></div>
        <div class="wing__r"></div>
        <div class="wing__l"></div>
    </div>
    <div class="moth1">
        <div class="moth1__body"></div>
        <div class="wing1__r"></div>
        <div class="wing1__l"></div>
    </div>
    <div class="moth2">
        <div class="moth2__body"></div>
        <div class="wing2__r"></div>
        <div class="wing2__l"></div>
    </div>
    <div class="backdrop">
        <div class="lightbulbcontainer">
            <div class="lightbulb">
                <div class="lightbulb__wire"></div>
                <div class="lightbulb__metal">
                    <div class="metal__ring1"></div>
                    <div class="metal__ring2"></div>
                </div>
                <div class="lightbulb__top"></div>
                <div class="lightbulb__bulb">
                    <div class="lightbulb__on"></div>
                    <div class="bulb__coil">
                        <div class="coil__side1"></div>
                        <div class="coil__side2"></div>
                        <div class="coil__bottom"></div>
                        <div class="lightbulb__shine"></div>
                    </div>
                </div>
                <div class="light"></div>
            </div>

        </div>

    </div>


    <div class="lightstring">
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__bead"></div>
        <div class="string__ring"></div>
    </div>

</body>
...
```
#css
```
html,
body,
div {
    border: 0;
    padding: 0;
    margin: 0;
}

.body {
    height: 100vh;
    width: 100vw;
    display: flex;
    justify-content: center;
    align-items: center;
}

.moth,
.moth1,
.moth2 {
    display: none;
}

.moth--visible {
    display: initial;
    height: 20vmin;
    position: relative;
    top: -12vmin;
    left: 32vmin;
    animation-name: moth--visible;
    animation-duration: 100ms;
    animation-timing-function: ease-in-out;
    animation-fill-mode: forwards;
    z-index: 2;
}

.moth1 {
    right: 22vmin;
    bottom: 6vmin;
}

.moth2 {
    right: 15vmin;
    top: -8vmin;
}

.moth__body,
.moth1__body,
.moth2__body {
    height: 2vmin;
    width: 0.4vmin;
    border-radius: 100vmin;
    background-color: rgba(0, 0, 0, 0.836);
    position: absolute;
    right: -0.2vmin;
    bottom: 0vmin;
}

.wing__r,
.wing__l,
.wing1__r,
.wing1__l,
.wing2__r,
.wing2__l {
    height: 2vmin;
    width: 2vmin;
    border-radius: 100%;
    background-color: rgba(128, 0, 128, 0.7);
    position: absolute;
    bottom: 0.05vmin;
    right: -0.1vmin;
    animation-name: moth--flutter;
    animation-duration: 300ms;
    animation-direction: alternate-reverse;
    animation-timing-function: ease-in-out;
    animation-iteration-count: infinite;
    z-index: -2;
}

.wing__l,
.wing1__l,
.wing2__l {
    left: 0vmin;
}

.wing1__r,
.wing1__l {
    background-color: rgb(101, 14, 182, 0.7);
}

.wing2__r,
.wing2__l {
    background-color: rgb(19, 139, 187, 0.7);
}

.moth--fly {
    animation-name: moth--fly;
    animation-duration: 10s;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
}

.moth--fly1 {
    animation-name: moth--fly1;
    animation-duration: 10s;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
}

.moth--fly2 {
    animation-name: moth--fly2;
    animation-duration: 10s;
    animation-timing-function: ease-in-out;
    animation-iteration-count: infinite;
}

.backdrop {
    height: 70vmin;
    width: 70vmin;
    border-radius: 100%;
    border: 1vmin solid black;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: black;
    z-index: 0;
}

.lightbulbcontainer {
    height: 75vmin;
    display: flex;
    justify-content: center;
    align-items: center;
}

.light {
    height: 43.5vmin;
    width: 52vmin;
    border-radius: 100%;
    z-index: -1;
    position: relative;
    bottom: 30vmin;
    filter: blur(8vmin);
    background-color: rgb(94, 92, 92);
}

.light--glowon {
    animation-name: light--glow;
    animation-duration: 250ms;
    animation-timing-function: ease-in;
    animation-fill-mode: forwards;
}

.lightbulb {
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    position: relative;
    top: 5vmin;
}

.lightbulb__bulb {
    height: 17vmin;
    width: 17vmin;
    border-radius: 70%;
    /* border-bottom: 1vmin solid #b6c0c2; */
    border: .8vmin solid #b6c0c2;
    background-color: #d8e5e7;
    position: relative;
    bottom: 1.8vmin;
}

.lightbulb__bulb--light {
    animation-name: lightbulb__bulb--light;
    animation-duration: 100ms;
    animation-timing-function: linear;
    animation-fill-mode: forwards;
}

.lightbulb__top {
    height: 6vmin;
    width: 8vmin;
    border-top-left-radius: 50%;
    border-top-right-radius: 50%;
    border-right: .8vmin solid #b6c0c2;
    border-left: .8vmin solid #b6c0c2;
    background-color: #d8e5e7;
    z-index: 1;
}

.lightbulb__top--light {
    animation-name: lightbulb__top--light;
    animation-duration: 100ms;
    animation-timing-function: linear;
    animation-fill-mode: forwards;
}

.lightbulb__metal {
    height: 7vmin;
    width: 10.5vmin;
    border-radius: 30%;
    background-color: #989792;
    position: relative;
    top: 2.5vmin;
    z-index: 2;
}

.lightbulb__metal--shine {
    animation-name: lightbulb__metal--shine;
    animation-duration: 100ms;
    animation-timing-function: linear;
    animation-fill-mode: forwards;
}

.metal__ring1,
.metal__ring2 {
    height: .5vmin;
    width: 11vmin;
    border-radius: 100px;
    background-color: #52514e;
    position: relative;
    transform: rotate(-5deg);
    right: 0.25vmin;
}

.metal__ring1 {
    top: 4vmin;
}

.metal__ring2 {
    top: 2vmin;
}

.lightbulb__wire {
    height: 15vmin;
    width: .75vmin;
    background-color: black;
    position: relative;
    top: 4.5vmin;
}

.bulb__coil {
    position: relative;
    bottom: 2.6vmin;
    left: 6.5vmin;
    z-index: 1;
}

.coil__side1,
.coil__side2 {
    height: 10.5vmin;
    width: 0.3vmin;
    background-color: rgb(61, 60, 60);
    transform: rotate(10deg);
}

.coil__sides--light {
    animation-name: coil__sides--light;
    animation-duration: 100ms;
    animation-timing-function: linear;
    animation-fill-mode: forwards;
}

.coil__side2 {
    transform: rotate(-10deg);
    position: absolute;
    top: 0vmin;
    left: 4vmin;
}

.coil__bottom {
    width: 5.9vmin;
    height: 3vmin;
    border-radius: 100%;
    border-bottom: 0.8vmin solid rgb(61, 60, 60);
    position: absolute;
    top: 8vmin;
    left: -0.8vmin;
}

.coil__bottom--hot {
    animation-name: coil__bottom--hot;
    animation-duration: 100ms;
    animation-timing-function: linear;
    animation-fill-mode: forwards;
}

.lightbulb__shine {
    height: 12vmin;
    width: 12vmin;
    border-radius: 100%;
    background-color: rgba(248, 248, 255, 0.253);
    position: relative;
    bottom: 3.5vmin;
    right: 3vmin;
    animation-name: lightbulb--shine;
    animation-duration: 5s;
    animation-timing-function: linear;
    animation-fill-mode: forwards;
}

.lightstring {
    position: relative;
    bottom: 14vmin;
    right: 20vmin;
}

.string--pullon {
    animation-name: string--pull;
    animation-duration: 150ms;
    animation-timing-function: ease-in-out;
}

.string--pulloff {
    animation-name: string--pulloff;
    animation-duration: 150ms;
    animation-timing-function: ease-in-out;
}

.string__bead {
    height: 1vmin;
    width: 1vmin;
    border-radius: 100%;
    background-color: black;
    position: relative;
}

.string__ring {
    height: 2.5vmin;
    width: 2.5vmin;
    border-radius: 100% 100% 0 0;
    background-color: black;
    position: relative;
    right: 0.7vmin;
}

@keyframes moth--flutter {
    0% {
        width: 2vmin;
    }
    100% {
        width: 0.5vmin;
    }
}

@keyframes moth--fly {
    from {
        transform: rotate(0deg) translateX(4vmin) rotate(0deg);
    }
    to {
        transform: rotate(-360deg) translateX(4vmin) rotate(360deg);
    }
}

@keyframes moth--fly1 {
    from {
        transform: rotate(0deg) translateX(8vmin) rotate(0deg);
    }
    to {
        transform: rotate(360deg) translateX(8vmin) rotate(-360deg);
    }
}

@keyframes moth--fly2 {
    from {
        transform: rotate(0deg) translateX(-9vmin) rotate(0deg);
    }
    to {
        transform: rotate(-360deg) translateX(-9vmin) rotate(360deg);
    }
}

@keyframes moth--visible {
    0% {
        background-color: transparent;
    }
    100% {
        background-color: black;
    }
}

@keyframes light--glow {
    0% {
        background-color: rgb(94, 92, 92);
    }
    100% {
        background-color: #f4bf10;
    }
}

@keyframes lightbulb__bulb--light {
    from {
        background-color: #d8e5e7;
    }
    to {
        background-color: #f4bf10;
        border: .8vmin solid #dd9401;
    }
}

@keyframes lightbulb__top--light {
    0% {
        background-color: #d8e5e7;
    }
    100% {
        background-color: #f4bf10;
        border-right: .8vmin solid #dd9401;
        border-left: .8vmin solid #dd9401;
    }
}

@keyframes lightbulb--shine {
    0% {
        background-color: rgba(248, 248, 255, 0.253);
    }
    100% {
        filter: blur(0.5vmin);
    }
}

@keyframes lightbulb__metal--shine {
    0% {
        background-color: #989792;
    }
    100% {
        background-color: #5f5e5b;
    }
}

@keyframes coil__sides--light {
    0% {
        background-color: rgb(61, 60, 60);
    }
    100% {
        background-color: #dd9401;
    }
}

@keyframes coil__bottom--hot {
    0% {
        border-bottom: 0.8vmin solid rgb(61, 60, 60);
    }
    100% {
        background-color: #fff9f6;
        border-bottom: 0.8vmin solid #fff9f6;
        filter: blur(0.8vmin);
    }
}

@keyframes lightbulb__metal--shine {
    0% {
        background-color: #989792;
    }
    100% {
        background-color: #5f5e5b;
    }
}

@keyframes string--pull {
    from {
        transform: translateY(0);
    }
    to {
        transform: translateY(2vmin);
    }
}

@keyframes string--pulloff {
    from {
        transform: translateY(0);
    }
    to {
        transform: translateY(2vmin);
    }
}
```
#3 js
```
window.addEventListener("load", function () {
    const image = document.querySelector('.backdrop');
    const string = document.querySelector('.lightstring');
    image.addEventListener("click", animationListener);
    string.addEventListener("click", animationListener);

});

function animationListener(e) {
    const light = document.getElementsByClassName("light")[0];
    light.classList.toggle("light--glowon");
    const lightstring = document.getElementsByClassName("lightstring")[0];
    if (!lightstring.classList.contains("string--pulloff") && !lightstring.classList.contains("string--pullon")) {
        lightstring.classList.add("string--pullon");
    } else {
        lightstring.classList.toggle("string--pullon")
        lightstring.classList.toggle("string--pulloff");
    };

    const onClass = [
        ["lightbulb__bulb", "lightbulb__bulb--light"],
        ["lightbulb__top", "lightbulb__top--light"],
        ["lightbulb__metal", "lightbulb__metal--shine"],
        ["coil__side1", "coil__sides--light"],
        ["coil__side2", "coil__sides--light"],
        ["coil__bottom", "coil__bottom--hot"],
        ["moth", "moth--visible"],
        ["moth1", "moth--visible"],
        ["moth2", "moth--visible"],
        ["moth", "moth--fly"],
        ["moth1", "moth--fly1"],
        ["moth2", "moth--fly2"]
    ];


    onClass.forEach(function (a) {
        document.getElementsByClassName(a[0])[0].classList.toggle(a[1]);
    })
};
```
