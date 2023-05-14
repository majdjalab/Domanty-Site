<script>
export default {
    name: 'RippleButton'
};
</script>

<template>
    <a href="https://github.com/majdjalab/Domanty-React-Native-Chat-App" target="_blank" rel="noopener noreferrer" class="href">
        <div class="request-loader">
            <span>Source Code</span>
            <img src="/down-arrow.png" alt="">
            <div class="ring"></div>
            <div class="ring delay"></div>
        </div>
    </a>
</template>


<style>
.href{
    text-decoration: none;
}
.request-loader {
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 110px;
    width: 110px;
    color: #222;
    border-radius: 100%;
    background: #FFFFFF;
    box-shadow: 0 0 26px 0 rgba(0, 0, 0, 0.25);
    text-align: center;
}

.request-loader span {
    position: relative;
    font-size: 18px;
    justify-content: center;
    align-items: center;
}
.request-loader img{
    width: 20%;
}
.request-loader .ring {
    opacity: 0;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    position: absolute;
    top: -8px;
    left: -8px;
    right: 0;
    bottom: 0;
    content: '';
    height: 100%;
    width: 100%;
    border: 8px solid #2E86C1;
    border-radius: 100%;
    animation-name: ripple;
    animation-duration: 3s;
    animation-iteration-count: infinite;
    animation-timing-function: cubic-bezier(.65, 0, .34, 1);
    z-index: -1;
}

.request-loader .ring.delay {
    animation-delay: 0.5s;
}

@keyframes ripple {
    from {
        opacity: 1;
        transform: scale3d(0.75, 0.75, 1);
    }

    to {
        opacity: 0;
        transform: scale3d(1.5, 1.5, 1);
    }
}
</style>
