<template>
    <section id="skill">
        <div class="skill__inner">
            <h2 class="skill__title">
                challenge <em>나의 도전</em>
            </h2>
            <div class="skill__desc">
                <div>
                    <span>1.</span>
                    <h3>꿈을 설계하고 디자인하다.</h3>
                    <p>
                        저의 목표는 뛰어난 사용자 경험을 제공하고 웹 기술을
                        활용하여 혁신적인 프론트엔드 솔루션을 개발하는 것입니다.
                        다양한 플랫폼에서 원활하게 작동하는 모던 웹 애플리케이션을
                        제작하고, 사용자의 요구를 충족시키는
                        디자인을 구현하고자 합니다.
                    </p>
                </div>
                <div>
                    <span>2.</span>
                    <h3>나의 의지</h3>
                    <p>
                        저의 의지는 지속적인 학습과 기술적 성장을 향상시키는 데 있습니다.
                        업계의 변화를 주시하고, 최신 프론트엔드 기술과 트렌드를 습득하기
                        위해 노력하겠습니다. 어떤 어려움도 극복하고, 더 나은 사용자 경험을
                        위해 끊임없이 자기 계발하고 혁신을 추구하겠습니다.
                    </p>
                </div>
                <div>
                    <span>3.</span>
                    <h3>나의 장점</h3>
                    <p>
                        저의 강점 중 하나는 사용자 중심의 디자인을 개발하는 데 있습니다.
                        사용자 경험을 개선하고, 직관적이며 반응형 인터페이스를 디자인하며,
                        사용자 피드백을 반영하여 웹 애플리케이션을 개선할 것입니다.
                    </p>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
.skill__inner {
    padding: 16px;
    display: flex;
    justify-content: space-between;
}

.skill__title {
    position: sticky;
    top: 65px;
    left: 0;
    width: 48%;
    height: 4.9vw;
    font-size: 4vw;
    font-weight: 900;
    line-height: 1.6;
    text-transform: uppercase;
    font-family: var(--mainEng2-font);
    border-bottom: 0.4vw solid var(--mainFont-color);
    color: var(--mainFont-color);
}

.skill__title em {
    font-family: var(--mainKor-font);
    font-size: 1.25rem;
    font-weight: 400;
    display: inline-block;
    vertical-align: 4px;
}

.skill__desc {
    width: 50%;
}

.skill__desc span {
    font-size: 5vw;
    line-height: 1.5;
    font-weight: 900;
    font-family: var(--mainNum-font);
    color: var(--mainFont-color);
}

.skill__desc h3 {
    font-size: 1.5rem;
    text-decoration: underline;
    text-underline-position: under;
    font-weight: 600;
    margin-bottom: 1vw;
    font-family: var(--mainKor-font);
    color: var(--mainFont-color);
}

.skill__desc p {
    margin-bottom: 30vh;
    font-size: 1.1rem;
    font-family: var(--mainKor-font);
    color: var(--mainFont-color);
}

@media(max-width: 800px) {
    .skill__inner {
        flex-direction: column;
    }

    .skill__title {
        width: 100%;
        margin-bottom: 10vw;
        height: auto;
        background-color: var(--mainBg-color);
        font-size: 40px;
        line-height: 1.4;
    }

    .skill__desc {
        width: 100%;
    }

    .skill__desc span {
        font-size: 10vw;
    }

    .skill__desc p {
        font-size: 2vw;
    }
}
</style>