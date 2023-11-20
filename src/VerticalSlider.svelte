<style lang="scss">
    @import 'mixins';

    $item-height: 20vh;
    $animation-time: 20s;
    $items-qty: 5;
    $animation-delay-basic-value: calc($animation-time / $items-qty);
    @debug($animation-delay-basic-value);

    .wrapper {
        min-height: 100vh;
        @include flex-center;
    }

    .slider {
        @include flex-column;
        position: relative;
        gap: 1rem;
        width: 80%;
        height: $item-height * 3;
    }

    .item {
        @include flex-center;
        position: absolute;
        top: calc(50% - $item-height / 2);
        width: 100%;
        height: $item-height;
        background: #fff;
        border-radius: 10px;
        padding: 20px;
        opacity: 0;
        animation: scroll $animation-time linear infinite
    }

    .item:first-child {
        animation-delay: calc($animation-delay-basic-value * -1);
    }

    .item:nth-child(2) {
        animation-delay: calc($animation-delay-basic-value * 0);
    }

    .item:nth-child(3) {
        animation-delay: calc($animation-delay-basic-value * 1);
    }

    .item:nth-child(4) {
        animation-delay: calc($animation-delay-basic-value * 2);
    }

    .item:last-child {
        animation-delay: calc($animation-delay-basic-value * -2);
    }

    .icon {
        @include flex-center;
        width: 100px;
        height: 100px;
        flex-shrink: 0;
        font-size: 4rem;
    }

    .info {
        width: 100%;
        text-align: end;
    }

    .title {
        font-size: 2rem;
        text-transform: uppercase;
        margin-bottom: 1rem;
    }

    .link {
        display: block;
        color: inherit;
        text-decoration: none;
        font-size: 1.2rem;
    }

    @keyframes scroll {
        0% {
            opacity: 0;
            transform: translateY(100%) scale(.5);
            visibility: hidden;
        }

        4%, 20% {
            opacity: .36;
            transform: translateY(100%) scale(.7);
            visibility: visible;
        }
        24%, 40% {
            opacity: 1;
            transform: translateY(0) scale(1);
            visibility: visible;
        }

        44%, 60% {
            opacity: .36;
            transform: translateY(-100%) scale(.7);
            visibility: visible;
        }

        64%, 80% {
            opacity: 0;
            transform: translateY(-100%) scale(.5);
            visibility: hidden;
        }

        100% {
            opacity: 0;
            transform: translateY(-100%) scale(.5);
            visibility: hidden;
        }
    }
</style>

<div class="wrapper">
    <div class="slider">
        <div class="item">
            <div class="icon">
                <i class="fa-solid fa-hand-fist"></i>
            </div>
            <div class="info">
                <div class="title">Title</div>
                <a class="link" href="#">Link</a>
            </div>
        </div>
        <div class="item">
            <div class="icon">
                <i class="fa-solid fa-chess"></i>
            </div>
            <div class="info">
                <div class="title">Another title</div>
                <a class="link" href="#">Link</a>
            </div>
        </div>
        <div class="item">
            <div class="icon">
                <i class="fa-solid fa-dice-d20"></i>
            </div>
            <div class="info">
                <div class="title">Third title</div>
                <a class="link" href="#">Link</a>
            </div>
        </div>
        <div class="item">
            <div class="icon">
                <i class="fa-solid fa-dungeon"></i>
            </div>
            <div class="info">
                <div class="title">Title zaebal</div>
                <a class="link" href="#">Link</a>
            </div>
        </div>
        <div class="item">
            <div class="icon">
                <i class="fa-solid fa-dragon"></i>
            </div>
            <div class="info">
                <div class="title">Last title</div>
                <a class="link" href="#">Link</a>
            </div>
        </div>
    </div>
</div>