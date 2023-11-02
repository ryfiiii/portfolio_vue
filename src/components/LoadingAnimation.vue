<template>
    <div class="bg">
        <div class="pacman">
            <div></div>
            <div></div>
            <div></div>
            <div></div>
            <div></div>
        </div>
    </div>
</template>

<style scoped>
.bg {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    background-color: rgb(92, 180, 232);
    width: 100%;
    height: 100vh;
    position: absolute;
    transition: opacity 1s;
    z-index: 100;
}

/*-------------------------------------*/
/* Pacman Animation */
/*------------------------------------ */
.square-spin>div {
    -webkit-animation-fill-mode: both;
    animation-fill-mode: both;
    width: 50px;
    height: 50px;
    background: #fff;
    -webkit-animation: square-spin 3s 0s cubic-bezier(0.09, 0.57, 0.49, 0.9) infinite;
    animation: square-spin 3s 0s cubic-bezier(0.09, 0.57, 0.49, 0.9) infinite;
}

@-webkit-keyframes rotate_pacman_half_up {
    0% {
        -webkit-transform: rotate(270deg);
        transform: rotate(270deg);
    }

    50% {
        -webkit-transform: rotate(360deg);
        transform: rotate(360deg);
    }

    100% {
        -webkit-transform: rotate(270deg);
        transform: rotate(270deg);
    }
}

@keyframes rotate_pacman_half_up {
    0% {
        -webkit-transform: rotate(270deg);
        transform: rotate(270deg);
    }

    50% {
        -webkit-transform: rotate(360deg);
        transform: rotate(360deg);
    }

    100% {
        -webkit-transform: rotate(270deg);
        transform: rotate(270deg);
    }
}

@-webkit-keyframes rotate_pacman_half_down {
    0% {
        -webkit-transform: rotate(90deg);
        transform: rotate(90deg);
    }

    50% {
        -webkit-transform: rotate(0deg);
        transform: rotate(0deg);
    }

    100% {
        -webkit-transform: rotate(90deg);
        transform: rotate(90deg);
    }
}

@keyframes rotate_pacman_half_down {
    0% {
        -webkit-transform: rotate(90deg);
        transform: rotate(90deg);
    }

    50% {
        -webkit-transform: rotate(0deg);
        transform: rotate(0deg);
    }

    100% {
        -webkit-transform: rotate(90deg);
        transform: rotate(90deg);
    }
}

@-webkit-keyframes pacman-balls {
    75% {
        opacity: 0.7;
    }

    100% {
        -webkit-transform: translate(-100px, -6.25px);
        transform: translate(-100px, -6.25px);
    }
}

@keyframes pacman-balls {
    75% {
        opacity: 0.7;
    }

    100% {
        -webkit-transform: translate(-100px, -6.25px);
        transform: translate(-100px, -6.25px);
    }
}

.pacman {
    position: relative;
    transform: scale(2);
}

.pacman>div:nth-child(2) {
    -webkit-animation: pacman-balls 1s -0.99s infinite linear;
    animation: pacman-balls 1s -0.99s infinite linear;
}

.pacman>div:nth-child(3) {
    -webkit-animation: pacman-balls 1s -0.66s infinite linear;
    animation: pacman-balls 1s -0.66s infinite linear;
}

.pacman>div:nth-child(4) {
    -webkit-animation: pacman-balls 1s -0.33s infinite linear;
    animation: pacman-balls 1s -0.33s infinite linear;
}

.pacman>div:nth-child(5) {
    -webkit-animation: pacman-balls 1s 0s infinite linear;
    animation: pacman-balls 1s 0s infinite linear;
}

.pacman>div:first-of-type {
    width: 0px;
    height: 0px;
    border-right: 25px solid transparent;
    border-top: 25px solid #fff;
    border-left: 25px solid #fff;
    border-bottom: 25px solid #fff;
    border-radius: 25px;
    -webkit-animation: rotate_pacman_half_up 0.5s 0s infinite;
    animation: rotate_pacman_half_up 0.5s 0s infinite;
    position: relative;
    left: -30px;
}

.pacman>div:nth-child(2) {
    width: 0px;
    height: 0px;
    border-right: 25px solid transparent;
    border-top: 25px solid #fff;
    border-left: 25px solid #fff;
    border-bottom: 25px solid #fff;
    border-radius: 25px;
    -webkit-animation: rotate_pacman_half_down 0.5s 0s infinite;
    animation: rotate_pacman_half_down 0.5s 0s infinite;
    margin-top: -50px;
    position: relative;
    left: -30px;
}

.pacman>div:nth-child(3),
.pacman>div:nth-child(4),
.pacman>div:nth-child(5),
.pacman>div:nth-child(6) {
    background-color: #fff;
    width: 15px;
    height: 15px;
    border-radius: 100%;
    margin: 2px;
    width: 10px;
    height: 10px;
    position: absolute;
    -webkit-transform: translate(0, -6.25px);
    transform: translate(0, -6.25px);
    top: 25px;
    left: 70px;
}</style>