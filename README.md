# Just-for-fun
Why coding without interest 😄

# List
## loading-square
<style>
    .container {
        margin: 0;
        width: 100%;
        height: 100%;
        overflow: hidden;
    }
    .container {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    h1 {
        font-family: "Helvetica", "Arial", sans-serif;
        font-size: 1.05rem;
    }

    .logo {
        position: relative;
        width: 100px;
        height: 100px;
        box-sizing: border-box;
        background-color: white;
    }

    .logo::before,
    .logo::after {
        content: "";
        position: absolute;
        width: 100%;
        height: 100%;
        box-sizing: border-box;
        border: 4px solid transparent;
        animation-timing-function: linear;
    }

    .logo::before {
        top: 0;
        left: 0;
        border-top-color: #000;
        border-right-color: #000;
        animation: border-before 1.5s infinite;
        animation-direction: alternate;
    }

    .logo::after {
        bottom: 0;
        right: 0;
        border-left-color: #000;
        border-bottom-color: #000;
        animation: border-after 1.5s infinite;
        animation-direction: alternate;
    }

    .logo > div {
        position: absolute;
    }

    .red {
        top: 4px;
        bottom: 0;
        left: 0;
        border-right: 4px solid #000;
        background-color: #ea5664;
        animation: red 1.5s infinite;
        animation-direction: alternate;
    }

    .orange {
        bottom: 0;
        left: 27%;
        right: 4px;
        border-top: 4px solid #000;
        background-color: #f3b93f;
        animation: orange 1.5s infinite;
        animation-direction: alternate;
    }

    .white {
        right: 5px;
        top: 4px;
        bottom: 50%;
        height: 50%;
        border-left: 4px solid #000;
        background-color: #fff;
        animation: white 1.5s infinite;
        animation-direction: alternate;
    }
    

    @keyframes border-before {
        0% {
            width: 0;
            height: 0;
            border-right-color: transparent;
        }
        5.99% {
            border-right-color: transparent;
        }
        12% {
            height: 0;
            width: 100%;
            border-right-color: #000;
        }
        25%,
        100% {
            width: 100%;
            height: 100%;
        }
    }

    @keyframes border-after {
        0%,
        24.99% {
            width: 0;
            height: 0;
            border-left-color: transparent;
            border-bottom-color: transparent;
        }
        25% {
            border-bottom-color: #000;
        }
        37% {
            height: 0;
            width: 100%;
            border-left-color: #000;
        }
        50%,
        100% {
            width: 100%;
            height: 100%;
        }
    }

    @keyframes red {
        0%,
        50% {
            width: 0;
            opacity: 0;
        }
        50.01% {
            opacity: 1;
        }
        65%,
        100% {
            width: 27%;
            opacity: 1;
        }
    }

    @keyframes orange {
        0%,
        65% {
            height: 0;
            opacity: 0;
        }
        65.01% {
            opacity: 1;
        }
        80%,
        100% {
            height: 50%;
            opacity: 1;
        }
    }

    @keyframes white {
        0%,
        75% {
            width: 0;
            opacity: 0;
        }
        75.01% {
            opacity: 1;
        }
        90%,
        100% {
            width: 27%;
            opacity: 1;
        }
    }
</style>

<div class="container">
    <div class="logo">
        <div class="white"></div>
        <div class="orange"></div>
        <div class="red"></div>
    </div>
    <h1>Loading ...</h1>
</div>

## css-topnave
<style>
        ul{
            list-style: none;
            position: relative;
            display: flex;
            /* width: 800px; */
            
        }
        
        li{
            position: relative;
            padding: 20px;
            /* font-size: 24px; */
            color: #000;
            line-height: 1;
            transition: 0.2s all linear;
            cursor: pointer;
        }
        li::before {
            content: "";
            position: absolute;
            top: 0;
            left: 100%;
            width: 0;
            height: 100%;
            border-bottom: 2px solid #000;
            transition: 0.2s all linear;
        }
        li:hover::before {
            width: 100%;
            top: 0;
            left: 0;
            transition-delay: 0.1s;
            border-bottom-color: #000;
            z-index: -1;
        }
        li:hover ~ li::before {
            left: 0;
        }
        li:active {
            background: #000;
            color: #fff;
        }
</style>

<ul>
    <li>纯css</li>
    <li>很有趣</li>
    <li>光标下划线跟随</li>
    <li>topnav</li>
    <li>underline</li>
</ul>
