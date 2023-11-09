<script setup>
import { footerText } from "@/constants/index"
</script>

<template>
    <footer id="footer" role="contentinfo">
        <div class="footer__inner">
            <h2 class="footer__text">
                <div>rlanrider</div>
                <div>@rlan</div>
            </h2>
            <div class="footer__info">
                <div class="left">
                    <div class="title">
                        <a href="#">sign up</a>
                    </div>
                    <p class="desc">회원가입을 하시면 댓글과 게시판 기능을 이용할 수 있습니다.</p>
                </div>
                <div class="right">
                    <h3>social</h3>
                    <ul>
                        <li v-for="(text, key) in footerText" :key="key">
                            <a :href="text.link">{{ text.title }}</a>
                            <em>{{ text.desc }}</em>
                        </li>
                    </ul>
                </div>
            </div>
            <div class="footer__right">
                &copy; 2023 rlanrider<br />
                이 사이트는 비트를 이용하여 제작하였습니다.
            </div>
        </div>
    </footer>
</template>

<style lang="scss">
#footer {
    width: 100%;
}

.footer__inner {
    width: 100%;
    background-color: var(--mainBg-color);
    padding: 2.5vw;
    color: var(--subBg400);
}

.footer__text {
    text-align: center;
    font-size: 2rem;
    color: var(--subBg400);
    text-transform: uppercase;
    margin-bottom: 40px;
    border-bottom: 2px solid var(--subBg400);
    padding-bottom: 20px;
}

.footer__info {
    text-align: center;
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    margin-bottom: 40px;
}

.footer__info .left {
    width: 48%;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    text-align: left;
}

.footer__info .left .title {
    width: 100%;
    border-bottom: 1px solid var(--subBg400);
}

.footer__info .left .title a {
    text-align: left;
    text-transform: uppercase;
    color: var(--subBg400);
    font-size: 2rem;
    margin-bottom: 1rem;
    display: block;
    transition: all 0.2s;
}

.footer__info .left .title a:hover {
    transform: translateY(-10%);
    background-color: var(--mainBg2-color);
}

.footer__info .left .desc {
    margin-top: 10px;
    width: 100%;
    font-size: 1rem;
}

.footer__info .right {
    width: 50%;
}

.footer__info .right h3 {
    text-align: left;
    font-size: 2rem;
    text-transform: uppercase;
    margin-bottom: 16px;
}

.footer__info .right li {
    text-align: left;
    border-top: 1px solid var(--subBg400);
    padding: 10px 0;
    font-size: 1.1rem;
}

.footer__info .right em {
    opacity: 0;
    transition: opacity 0.4s;
}

.footer__info .right li:hover {
    cursor: pointer;
}

.footer__info .right li:hover em {
    opacity: 1;
}

.footer__info .right a {
    font-weight: 800;
    color: var(--subBg400);
    text-transform: uppercase;
}

.footer__right {
    text-align: center;
    font-size: 1rem;
}

@media(max-width: 800px) {
    .footer__info {
        justify-content: center;
        flex-direction: column;
    }

    .footer__info .left {
        width: 100%;
        margin-bottom: 20px;
    }

    .footer__info .right {
        width: 100%;
    }
}
</style>