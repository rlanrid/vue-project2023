<script setup>
import { siteText } from "@/constants/index"
</script>

<template>
    <section id="site">
        <div class="site__inner">
            <div class="site__title">
                Site Coding <em>나의 작업물</em>
            </div>
            <div class="site__wrap">
                <div :class="['site__item', 's' + (key + 1)]" v-for="(site, key) in siteText" :key="key">
                    <span class="num">{{ key + 1 }}.</span>
                    <div class="text">
                        <div>{{ site.text[0] }}</div>
                        <div>{{ site.text[1] }}</div>
                        <div>{{ site.text[2] }}</div>
                    </div>
                    <h3 class="title">
                        {{ site.title }}
                    </h3>
                    <div class="btn">
                        <a :href="site.code">code</a>
                        <a :href="site.view">view</a>
                    </div>
                    <div class="info">
                        <span>{{ site.info[0] }}</span>
                        <span>{{ site.info[1] }}</span>
                        <span>{{ site.info[2] }}</span>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
.site__inner {
    padding: 16px;
    display: flex;
    flex-wrap: wrap;
}

.site__title {
    width: 48%;
    height: 5vw;
    font-size: 4vw;
    font-weight: 900;
    line-height: 1.6;
    text-transform: uppercase;
    font-family: var(--mainEng2-font);
    border-bottom: 0.4vw solid var(--mainFont-color);
    color: var(--mainFont-color);
    margin-bottom: 2vw;
    position: sticky;
    left: 0;
    top: 70px;
}

.site__title em {
    font-family: var(--mainKor-font);
    font-size: 1.25rem;
    font-weight: 400;
    display: inline-block;
    vertical-align: 4px;
}

.site__wrap {
    width: 100%;
}

.site__item {
    padding: 70px;
    margin-bottom: 2vw;
    border-radius: 20px;
    position: sticky;
    left: 0;
}

.site__item.s1 {
    background-color: var(--subBg100);
    top: 180px;
}

.site__item.s2 {
    background-color: var(--subBg200);
    top: 200px;
}

.site__item.s3 {
    background-color: var(--subBg300);
    top: 220px;
}

.site__item.s4 {
    background-color: var(--subBg400);
    top: 240px;
}

.site__item .num {
    text-align: left;
    font-size: 3.25vw;
    font-family: var(--mainNum-font);
    color: var(--mainBg-color);
}

.site__item .text {
    width: 100%;
    text-align: center;
    text-transform: uppercase;
    font-weight: 900;
    font-size: 2.5vw;
    color: var(--mainBg-color);
}

.site__item h3 {
    text-align: center;
    font-size: 1.5rem;
    color: var(--subBg100);
    margin-bottom: 10px;
}

.site__item .btn {
    text-align: center;
    font-size: 1.25rem;
    color: var(--white100);
    font-family: var(--mainEng2-font);
}

.site__item .btn a {
    padding: 5px 15px;
    background-color: var(--subBg400);
}

.site__item .info {
    text-align: center;
    margin-top: 10px;
}

.site__item .info span {
    display: block;
    font-size: 1rem;
    color: var(--white100);
    font-family: var(--mainEng2-font);
}


@media (max-width: 800px) {
    .site__inner {
        flex-direction: column;
    }

    .site__title {
        width: 100%;
        margin-bottom: 10vw;
        height: auto;
        background-color: var(--mainBg-color);
        font-size: 40px;
        line-height: 1.4;
    }
}
</style>