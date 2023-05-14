<script>
import RippleButton from './RippleButton.vue';
import Content from './Content.vue';
import Footer from './Footer.vue';

export default {
    data: () => ({
        typeValue: "",
        typeStatus: false,
        typeArray: ["React Native Chat Application", "With Firebase as a Backend"],
        typingSpeed: 90,
        erasingSpeed: 70,
        newTextDelay: 2000,
        typeArrayIndex: 0,
        charIndex: 0
    }),
    methods: {
        typeText() {
            if (this.charIndex < this.typeArray[this.typeArrayIndex].length) {
                if (!this.typeStatus) {
                    this.typeStatus = true;
                }
                this.typeValue += this.typeArray[this.typeArrayIndex].charAt(this.charIndex);
                this.charIndex += 1;
                setTimeout(this.typeText, this.typingSpeed);
            }
            else {
                this.typeStatus = false;
                setTimeout(this.eraseText, this.newTextDelay);
            }
        },
        eraseText() {
            if (this.charIndex > 0) {
                if (!this.typeStatus) {
                    this.typeStatus = true;
                }
                this.typeValue = this.typeArray[this.typeArrayIndex].substring(0, this.charIndex - 1);
                this.charIndex -= 1;
                setTimeout(this.eraseText, this.erasingSpeed);
            }
            else {
                this.typeStatus = false;
                this.typeArrayIndex += 1;
                if (this.typeArrayIndex >= this.typeArray.length) {
                    this.typeArrayIndex = 0;
                }
                setTimeout(this.typeText, this.typingSpeed + 1000);
            }
        }
    },
    created() {
        setTimeout(this.typeText, this.newTextDelay + 200);
    },
    
    components: { RippleButton, Content, Footer }
};
</script>

<template>
  <div>
    <div class="header">
      <img class="center" src="/logo.png" />
    </div>
    <div class="full-screen">
      <div class="container">
        <div class="shape"></div>
        <img src="/mockupBg.svg">
        <div>
          <h1 class="title">DOMANTY</h1>
          <p class="main-title">
            Open Source
            <span class="typed-text">{{ typeValue }}</span>
            <span class="cursor" :class="{ 'typing': typeStatus }">&nbsp;</span>
          </p>
        </div>
      </div>
    </div>
    <div class="header-center">
      <RippleButton />
    </div>
    <div>
      <Content />
    </div>
    <div>
      <Footer />
    </div>
  </div>
</template>



<style scoped>
.full-screen {
  display: flex;
}
.header{
    display: block;
    text-align: center;
    margin: 0 ;
}
img.center{
  width: 10vw;
  text-align:center;
  margin-top: 2vw;
  padding:0px;
}
.title {
  background-image: url(/bg.svg);
  background-repeat: repeat;
  background-size: 100vw;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  will-change: filter;
  transition: filter 300ms;
  font-size: 13vw;
  font-weight: 1000;
  margin-bottom: 0%;
}

.container {
  display: flex;
  flex-direction: row;
  align-items: center;
}

.container img {
  width: 45%;
  margin-top: 8%;
}

.title {
  font-size: 13vw;
  font-weight: 1000;
  margin-bottom: 0%;
}

.main-title {
  font-size: 2.8vw;
  font-weight: normal;
  color: #222;
  margin-top: 0;
  margin-bottom: 0;
}

.typed-text {
  color: #2E86C1;
}

.cursor {
  display: inline-block;
  width: 2px;
  background-color: #2E86C1;
  animation: cursorBlink 1s infinite;
}

.cursor.typing {
  animation: none;
}

 .shape {
  width: 37vw;
  height: 37vw;
  background: #222;
  animation: wave 4.0s ease-in-out infinite;
  position: absolute;
  margin-top: 9.5%;
  margin-left: 4%;
  left: 0;
  z-index: -1;
}
  

.header-center {
  font-size: 2rem;
  color: #222;
  display: grid;
  grid-template-columns: 1fr max-content 1fr;
  grid-column-gap: 1.2rem;
  align-items: center;
  margin-bottom: 8%;
  margin-top: 5%;
  margin-right: 24%;
  margin-left: 22%;
}

.header-center::before,
.header-center::after {
  content: "";
  display: block;
  height: 1px;
  background-color: currentColor;
}

  @keyframes wave {
    0%, 100% {
      border-radius: 70% 30% 72% 28% / 27% 61% 39% 73%;
    }
    50% {
      border-radius: 77% 23% 54% 46% / 40% 38% 62% 60%;
    }
  }


/* The typing animation */
@keyframes cursorBlink {
  49% {
    background-color: #fff;
  }

  50% {
    background-color: transparent;
  }

  99% {
    background-color: transparent;
  }
}

@media (max-width: 768px) {
img.center{
  width: 25vw;
  text-align:center;
  margin-top: 4vw;
  padding:0px;
}
.title {
  font-size: 19vw;
  background-size: 100vw;
}

  .container {
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-left: 5vw;
  }

  .container img {
    width: 70vw;
    margin-bottom: 1vw;
  }
  .main-title {
  font-size: 4vw;
}
 .shape {
  width: 70vw;
  height: 60vw;
  background: #222;
  animation: wave 4.0s ease-in-out infinite;
  position: absolute;
  margin-bottom: 40vw;
  margin-left: 7vw;
  left: 0;
  z-index: -1;
}

.header-center {
  font-size: 2rem;
  color: #222;
  display: grid;
  grid-template-columns: 1fr max-content 1fr;
  grid-column-gap: 1.2rem;
  align-items: center;
  margin-bottom: 12%;
  margin-top: 15%;
  margin-right: 10%;
  margin-left: 8%;
}
  
}

</style>
