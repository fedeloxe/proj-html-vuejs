<script>
export default {
    data() {
        return {
            auto_play: null,
            activeImage: 0,
            slides: [
                {
                    image: "/slider-autocar-5.jpg",
                    title: "Buy And Sell Your Car At Its Value",
                    text: "Find the right price and dealer",
                },
                {
                    image: "/slider-autocar-6.jpg",
                    title: "The Easiest Way To Buy And Sell Vehicles",
                    text: "Find the right price and dealer",
                },
            ],
        };
    },
    methods: {
        changeImage(index) {
            this.activeImage = index;
        },
        next() {
            if (this.activeImage < this.slides.length - 1) {
                this.activeImage++;
            } else {
                this.activeImage = 0;
            }
        },
        prev() {
            if (this.activeImage > 0) {
                this.activeImage--;
            } else {
                this.activeImage = this.slides.length - 1;
            }
        },
        autoPlay() {
            this.auto_play = setInterval(() => {
                this.next();
            }, 3000);
        },
    },
    created() {
        this.autoPlay();
    },



};
</script>
<template lang="">
    <div class="carousel padding">
        <div class="container-fluid p-0">
          <div class="slider-wrapper">
            <div class="item">
              
              <img v-bind:src="slides[activeImage].image" v-bind:alt="slides.title" />
              <div class="text">
                <h2 class="my-4">{{ slides[activeImage].title }}</h2>
                <p class="fs-4">
                  {{ slides[activeImage].text }}
                </p>
                
                <button class="white">Learn More &rarr;</button>
              </div>
            </div>
            <div class="prev" @click="prev">❮</div>
            <div class="next" @click="next">❯</div>
          </div>
        </div>
    </div>
</template>
<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

.padding {
    padding-top: 100px;
}

.item {

    width: 100%;
    height: 90vh;
    position: relative;
}

.item img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.text {
    position: absolute;
    top: 45%;
    left: 30%;
    transform: translate(-50%, -50%);
    width: 600px;
    text-align: left;
    color: rgb(255, 255, 255);

    button {
        margin: 20px;
        height: 50px;
        width: 150px;
        border: none;
        color: $black;
        background-color: $white;
        font-weight: 700;
    }

    .white {
        color: $white;
        background-color: $black;
    }
}

.next,
.prev {
    font-size: 30px;
    padding: 10px 20px;
    position: absolute;
    top: 40%;
    transform: translate(-50%, -50%);
    cursor: pointer;
    z-index: 2;
    background-color: $black;
    color: $white;
}

.prev {
    left: 5%;
}

.next {
    right: 5%;
}
</style>



