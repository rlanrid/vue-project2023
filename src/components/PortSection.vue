<script setup>
import { portText } from "@/constants/index"
</script>

<template>
    <section id="port">
        <div class="port__inner">
            <div class="port__title">
                portfolio <em>포폴 작업물</em>
            </div>
            <div class="port__wrap">
                <div v-for="(port, key) in portText" :key="key" :class="['port__item', 'p' + (key + 1)]">
                    <span class="num">{{ port.num }}</span>
                    <a href="#">
                        <img :src="port.img" alt="이미지1">
                    </a>
                    <h3 class="title">{{ port.title }}</h3>
                    <p class="desc">
                        {{ port.desc }}
                    </p>
                    <div class="btn">
                        <a :href="port.code">사이트 보기</a>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import gsap from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";
gsap.registerPlugin(ScrollTrigger);

export default {
    mounted: function () {
        this.scrollAnimation();
    },
    methods: {
        scrollAnimation() {
            const horSection = gsap.utils.toArray(".port__item");

            gsap.to(horSection, {
                xPercent: -120 * (horSection.length - 1),
                ease: "none",
                scrollTrigger: {
                    trigger: "#port",
                    start: "top top",
                    end: "+=3000",
                    pin: true,
                    scrub: 1,
                    markers: true,
                    invalidateOnRefresh: true,
                    anticipatePin: 1,
                }
            });
        }
    }
}
</script>

<style lang="scss">
#port {
    width: 100%;
    overflow: hidden;
}

.port__inner {
    padding: 16px;
}

.port__wrap {
    display: flex;
    flex-wrap: wrap;
    width: 7000px;
}

.port__item {
    width: 500px;
    height: 70vh;
    background-color: var(--subBg100);
    margin-right: 20px;
    padding: 25px;
    transition: filter 0.4s;
}

.port__item:hover {
    filter: brightness(70%);
    cursor: pointer;
}

.port__title {
    width: 48%;
    height: 5vw;
    font-size: 4vw;
    font-weight: 900;
    line-height: 1.6;
    text-transform: uppercase;
    font-family: var(--mainEng2-font);
    border-bottom: 0.4vw solid var(--mainFont-color);
    color: var(--mainFont-color);
    margin-bottom: 4vw;
    position: sticky;
    left: 0;
    top: 70px;
}

.port__title em {
    font-family: var(--mainKor-font);
    font-size: 1.25rem;
    font-weight: 400;
    display: inline-block;
    vertical-align: 4px;
}

.port__item .num {
    text-align: left;
    font-size: 2vw;
    font-family: var(--mainNum-font);
    color: var(--white100);
}

.port__item .title {
    text-align: center;
    font-size: 1.5rem;
    color: var(--white200);
    border-bottom: 2px solid var(--white200);
    padding-bottom: 10px;
    font-weight: 800;
}

.port__item .desc {
    margin-top: 10px;
    color: var(--white200);
}

.port__item img {
    margin-bottom: 10px;
}

.port__item .btn {
    text-align: center;
    border: 1px solid var(--white200);
    padding: 10px 40px;
    margin-top: 15px;
    color: var(--white200);
}

@media(max-width: 800px) {
    .port__inner {
        flex-direction: column;
    }

    .port__title {
        width: 100%;
        margin-bottom: 10vw;
        height: auto;
        background-color: var(--mainBg-color);
        font-size: 40px;
        line-height: 1.4;
    }
}
</style>