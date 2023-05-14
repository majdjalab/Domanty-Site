<template>
    <div>
        <div class="contribute">
            <p class="title">How To Contribute?</p>
            <p class="contribute-desc">As an Open Source project, any developer can Contribute via Github,
                and for The Permissions Developers can learn or copy a part for their projects,
                but it's not allowed to use this project for profit purposes & it's not allowed to copy
                the entire UI or logo
            </p>
            <img src="/bottomDivider.svg" :style="{ width: '50%', marginTop: '0%' }" />
        </div>
        <div class="container">
            <h1 class="title">Tools And Technologies</h1>
            <div class="cards">
                <div class="card">
                    <img src="/react.svg" :style="{ width: '40%', margin: '4%' }" />
                    <div class="card-title">React Native (Front-End)</div>
                    <div class="card-text">React Native is a popular framework for building mobile applications for both
                        Android
                        and iOS platforms. It allows developers to use the same codebase for both platforms, saving time and
                        effort.
                        React Native offers a range of pre-built UI components that can be used to build complex user
                        interfaces
                        easily.
                    </div>
                </div>
                <div class="card">
                    <img src="/firebase.svg" :style="{ width: '40%', margin: '4%' }" />
                    <div class="card-title">Firebase (Back-End)</div>
                    <div class="card-text">Firebase offers a powerful and user-friendly back-end for authentication and
                        real-time database, enabling easy integration with React Native to build real-time apps with robust
                        back-end functionality. Learn to implement authentication and push,
                        delete, and retrieve data across multiple clients in real-time, a valuable skill for modern app
                        development.
                    </div>
                </div>
                <div class="card">
                    <img src="/expodev.png" :style="{ width: '40%', margin: '4%' }" />
                    <div class="card-title">Expo Dev (Simulator)</div>
                    <div class="card-text">To run your app on both Android and iOS platforms, you can use Expo Dev. It
                        provides
                        a real-time development experience, allowing you to see changes in your app immediately.
                        Additionally,
                        Expo Dev makes it easy to publish and share your app with other developers.
                    </div>
                </div>
            </div>
        </div>
        <div class="contribute">
            <p class="title">Try Live Demo</p>
            <img src="/qr-code.svg" :style="{ width: '50%', marginTop: '0%' }" />
        </div>
        <hr class="solid">
</div></template>



<style scoped>
.contribute {
    text-align: center;
    justify-content: center;
    align-items: center;
    margin-left: 20%;
    margin-right: 22%;
}
.contribute-desc{
    font-size: 28px;
    color: #222;
}
.title {
    color: #2e86c1;
    font-size: 3vw;
    font-weight: 1000;
    margin-bottom: 3%;
}

.container {
    font-size: 28px;
    text-align: center;
    justify-content: center;
    align-items: center;
    color: #222;
}

.cards {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    margin-top: 3%;
    margin-left: 5%;
    margin-right: 7%;
    margin-bottom: 5%;
}

.card {
    background-color: #fff;
    box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.2);
    border-radius: 10px;
    padding: 20px;
    margin: 10px;
    width: 25%;
    text-align: center;
    transition: box-shadow 0.3s ease;
}

.card:hover {
    box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.4);
}

.card-title {
    font-size: 20px;
    font-weight: bold;
    color: #2e86c1;
    margin-bottom: 10px;
}

.card-text {
    font-size: 18px;
    color: #222;
    margin-bottom: 8%;
}
.solid {
  border-top: 1px solid #222;
  margin-left: 12%;
  margin-right: 14%;
  margin-bottom: 2%;
}


@media (max-width: 768px) {


.contribute {
    text-align: center;
    justify-content: center;
    align-items: center;
    margin-left: 8%;
    margin-right: 10%;
}
.cards {
    display: block;
    margin-top: 3%;
    margin-left: 5%;
    margin-right: 7%;
    margin-bottom: 5%;
}

.card {
    background-color: #fff;
    box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.2);
    border-radius: 10px;
    width: 80%;
    text-align: center;
    transition: box-shadow 0.3s ease;
}

.title {
    color: #2e86c1;
    font-size: 8vw;
    font-weight: 1000;
    margin-bottom: 3%;
}
.contribute-desc{
    font-size: 20px;
    color: #222;
}
}
</style>
