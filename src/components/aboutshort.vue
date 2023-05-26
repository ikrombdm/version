<template>
    <main>
        <section id="about" class="mx-w">

            <h1 class="all-title">About</h1>

            <div class="about-short">


                <img :src="avatar" alt="">

                <div class="about-card">

                    <a href="#projects" class="all-icon">
                        <i class="fa-solid fa-face-grin-stars" style="color: #000000;"></i>
                        <i class="fa-solid fa-caret-down"></i>
                    </a>

                    <h1 class="about-header">
                        hello.
                    </h1>

                    <p class="about-title">My name is <span>Ikrombek.</span></p>

                    <article class="about-content">
                        I am an independent developer currently based in Uzbekistan. Most of my work is creating
                        <a href="#projects">landing page </a>,
                        SPA, CMS and publicly available code on
                        <a href="https://github.com/letsmailikrombek" target="_blank" rel="noopener noreferrer">
                            GitHub.•°
                        </a>
                    </article>
                </div>
            </div>

        </section>
    </main>
</template>
<script>
import avatar from "@/assets/image/avatar.png"

export default {
    data() {
        return {
            avatar,
        }
    },
}
</script>

<style lang="scss" scoped>
section {
    margin-top: 4rem;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center !important;
    height: 100vh;
    gap: 1rem;
    -webkit-font-smoothing: antialiased;
    padding: 20px;

    .about-short {
        margin-top: 4rem;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 5rem;
        line-height: 20px;

        img {
            width: 200px;
            height: 200px;
            background: #00000088;
            border-radius: 50%;
            padding: 15px;
        }

        .about-card {
            position: relative;
            width: 100%;
            padding: 2rem;
            background: #00000038;
            border: 2px solid #eee;
            border-radius: 12px;

            .about-header {
                color: #ffa200;
                margin-bottom: 20px;
                text-transform: uppercase;
                font-size: 2rem;
                letter-spacing: 0.8px;
            }

            .about-title {
                color: #eee;
                margin-bottom: 20px;
                text-transform: uppercase;
                letter-spacing: 0.5px;

                span {
                    color: #ffffff;
                    font-weight: bold;
                }
            }

            .about-content {
                color: #ede7e2e3;
                margin-bottom: 15px;
                line-height: 25px;

                a {
                    position: relative;
                    color: #fff;
                    transition: 0.1s ease-in;
                }

                a:hover::before {
                    height: 115%;
                    background: #ff9d00f0;
                }

                a:hover {
                    color: #000;
                }

                a::before {
                    position: absolute;
                    content: "";
                    height: 10px;
                    width: 105%;
                    left: -1px;
                    bottom: -2px;
                    background: #fffdfb95;
                    z-index: -1;
                    transition: 0.1s ease-in;
                }
            }

        }
    }
}

</style>