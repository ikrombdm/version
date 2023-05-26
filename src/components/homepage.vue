<template>
    <main>
        <section>

            <img :src="avatar" alt="">
            <h1 class="my-name">Ikrombek Urazaliyev</h1>
            <div class="my-skill">
                I am a web developer
                <!-- <div class="skills">
                    <p>Front-end</p>
                    <p>Back-end</p>
                </div> -->
            </div>

            <div class="socials">
                <a href="https://t.me/peculiarofplaceofpeculiarworld" target="_blank">
                    <i class="fa-brands fa-telegram"></i>
                </a>
                <a href="tel://955402502">
                    <i class="fa-solid fa-phone"></i>
                </a>
                <a href="https://github.com/letsmailikrombek" target="_blank">
                    <i class="fa-brands fa-github"></i>
                </a>
                <a href="#about">
                    <i class="fa-solid fa-file" target="_blank"></i>
                </a>
            </div>

            <a href="#about" class="mouse-wheel">
            </a>
        </section>
    </main>
</template>
<script>
import avatar from "@/assets/image/avatar.png"

export default {
    data() {
        return {
            avatar
        }
    }
}
</script>

<style lang="scss" scoped>
section {
    position: relative;
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 0 auto;
    gap: 1rem;
    -webkit-font-smoothing: antialiased;
    line-height: 20px;

    img {
        width: 120px !important;
        height: 120px !important;
        background: #ffa200;
        box-shadow: inset 0 0 5px #ffffff72;
        border-radius: 50%;
        object-fit: cover;
        padding: 4px;
        border: 4px solid white;
    }

    .my-name {
        margin-top: 1rem;
        text-align: center;
        font-size: 1.6rem;
        background: -webkit-linear-gradient(20deg, #ff8000, #ff6a00);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
    }

    .my-skill {
        position: relative;
        text-align: center;
        font-size: 1.2rem;
        color: #fff;
        font-weight: bold;
        display: flex;
        overflow: hidden !important;
        height: 20px;

        .skills {
            margin-left: 4px;
            text-align: start;
            animation: anim 4s ease infinite;
            color: #889093;
        }

    }

    .socials {
        margin-top: 20px;
        display: flex;
        gap: 2rem;
        padding: 13px 22px;
        border-radius: 7px;
        border: 1px solid rgba(255, 255, 255, 0.369);

        a {

            i {
                color: #c3c0c0;
                font-size: 1.3rem !important;
                transition: .1s ease-in;
            }
        }

        a:hover {

            i {
                color: #ffffff;
                transform: scale(1.2);
            }
        }
    }

    .mouse-wheel {
        position: absolute;
        bottom: 30px;
        width: 23px;
        height: 32px;
        border: 2px solid #ffffff;
        border-radius: 20px;
    }

    .mouse-wheel::after {
        position: absolute;
        content: "";
        min-height: 7px !important;
        max-height: 7px !important;
        min-width: 7px !important;
        max-width: 7px !important;
        margin-left: 8px;
        margin-top: 8px;
        background: #ff8800;
        border-radius: 5px;
        animation: anim2 1.5s ease-out infinite;
    }
}

@keyframes anim2 {
    0% ,100%{
        margin-top: 8px;
    }

    50% {
        margin-top: 16px;
    }
}
</style>