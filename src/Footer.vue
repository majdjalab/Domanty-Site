<template>
    <div class="footer">
        <div class="top-section">
            <div class="image-and-text">
                <img src="/logo.png" style="width:140px; margin-top: 10px;">
                <p style="font-size: 20px; color: #222;">Developed by Majd Jalab</p>
            </div>
            <p class="copyright">
                Copyright Ⓒ 2023 Domanty. All Rights Reserved.<br>
                E-mail : majdjalab@gmail.com
            </p>
            <div class="social-media-icons">
                <a href="https://www.linkedin.com/in/majd-jalab/"><img src="/linkedin.png"></a>
                <a href="https://twitter.com/MAJDJALAB"><img src="/twitter.png"></a>
                <a href="https://www.instagram.com/majdjalab"><img src="/instagram.png"></a>
                <a href="https://github.com/majdjalab"><img src="/github.png"></a>
            </div>
        </div>
    </div>
</template>

<style scoped>

.footer {
    justify-content: center;
    align-items: center;
}

.top-section {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
}
.social-media-icons {
    display: flex;
    margin-right: 15%;
}

.social-media-icons a {
    margin: 0 10px;
}

.social-media-icons img {
    width: 3vw;
}

.social-media-icons a:hover img {
    filter: brightness(70%);
}

.developed-by {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 3%;
}

.copyright {
    text-align: center;
    color: #222;
    font-size: 17px;
}

.developed-by img {
    width: 5vw;
    margin-right: 1%;
}

.developed-by p {
    font-size: 24px;
    color: #222;
}

.image-and-text {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-left: 14%;
}

.image-and-text img {
    margin-bottom: 10px;
}


@media (max-width: 768px) {
    .footer {
    display: block;
    justify-content: center;
    align-items: center;
    }
  .top-section {
    display: block;
    justify-content: center;
    align-items: center;
}

.image-and-text {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-left: 0;
}

.social-media-icons {
    margin-right: 0;
    margin-top: 6%;
    justify-content: center;
}


.social-media-icons img {
    width: 6vw;
    margin-bottom: 50px;
}


}

</style>
