<template>
    <section class="mx-w">
        <h1 class="all-title3">Path</h1>

        <div class="about-mote-section">

            <div class="box">
                <div class="text">
                    <p>I am a front-end developer and ui/ux designer from Uzbekistan, Tashkent.
                        I have experience building SPAs and
                        JAMstack sites and a special interest in usability and web performance.
                        and sometimes posting my works on
                        <a href="https://www.youtube.com/channel/UCerbOYjJhYVWNMY9fPzCrVw" target="_blank">youtube.</a>
                    </p>
                </div>
                <div class="image">
                    <img :src="avatar" alt="log">
                </div>
            </div>
            <div class="box">
                <div class="image">
                    <img :src="step" alt="log">
                </div>
                <div class="text">
                    <h2><span class="span-color">F</span>irst steps.</h2>
                    <p>

                        I found programming in an online competition and became interested

                        Since then I have been learning programming online including udemy, youtube, personal websites.


                    </p>
                </div>
            </div>

            <div class="box">
                <div class="text">
                    <router-link class="link" to="/photos">
                        <i class="fa-solid fa-images"></i>
                    </router-link>
                    <h2><span class="span-color">P</span>hotography.</h2>
                    <p>
                        I have a passion for photography since I was a teenager. I love documentary and conceptual
                        photography but I mainly take portraits or travel photographs.
                    </p>
                </div>
                <div class="image">
                    <img :src="ph" alt="log">
                </div>
            </div>

        </div>

        <h1 class="title-main"><span class="span-color">E</span>ducation</h1>
        <div class="verti-section">

            <div class="verti-main">
                <div class="verti-item" v-for="education in educations" :key="education">
                    <p class="year">{{ education.years }}</p>
                    <div class="content-item">
                        <div class="-item-title">{{ education.title }}</div>
                        <div class="-item-name">{{ education.content }}</div>
                    </div>
                </div>
            </div>

        </div>


    </section>
</template>

<script>
import avatar from "@/assets/image/avatar.png"
import step from "@/assets/step.png"
import ph from "@/assets/ph.png"

export default {
    data() {
        return {
            avatar,
            step,
            ph,
            
            educations: [
                {
                    title: "School",
                    years: "2011-2021",
                    content: "Include collage"
                },
                {
                    title: "School",
                    years: "2011-2021",
                    content: "Include collage"
                },
            ]
        }
    },
}
</script>


<style lang="scss" scoped>
section {
    margin-top: 8rem;


    .span-color {
        color: #ffa200;
    }

    .about-mote-section {
        margin-top: 4rem;


        .box {
            display: flex;
            align-items: center;
            justify-content: center;
            grid-template-columns: 1fr 1fr;
            margin-top: 5rem;
            gap: 5rem;

            .text {
                position: relative;
                background: #00000055;
                padding: 1.2rem 1.5rem;
                border: 1px solid #ffa200;
                border-radius: 10px;

                h2 {
                    margin-bottom: 15px;
                    color: #fff;
                }

                p {
                    color: #ffffff;
                    font-size: 16px;
                    font-weight: 300;
                    line-height: 21px;
                    letter-spacing: .2px;
                    letter-spacing: 1px;

                    a {
                        position: relative;
                        color: #fff;
                        text-decoration: none;
                        font-weight: 400;
                    }

                    a:after {
                        position: absolute;
                        content: "";
                        left: 0;
                        bottom: 0;
                        height: 1px;
                        width: 100%;
                        background: #ffa200;
                        z-index: -1;
                        transition: 0.1s;
                    }

                    a:hover:after {
                        height: 100%;
                    }
                }

                .link {
                    position: absolute;
                    right: 10px;
                    top: 10px;
                    width: 30px;
                    height: 30px;
                    background: #ffa200;
                    border-radius: 5px;
                    display: flex;
                    justify-content: center;
                    align-items: center;
                    text-decoration: none;

                    i {
                        color: #000;
                    }
                }

                .link:hover {
                    background: #ffffff;
                }
            }

            .image {
                display: flex;
                align-items: center;
                justify-content: center;
            }

            .image img {
                width: 160px;
                user-select: none;
                -webkit-user-drag: none;
                opacity: 0.7;
            }
        }
    }

    .title-main {
        margin-top: 5rem;
        font-size: 1.2rem;
        color: #fff;

    }

    .verti-section {
        padding-bottom: 1rem;
        margin-top: 2rem;
        display: flex;
        gap: 1.5rem;
        overflow: scroll;

        .verti-main {
            display: flex !important;
            gap: 1.5rem;

            .verti-item {
                position: relative;
                height: 200px;
                width: 90px;
                min-width: 90px;
                background: #00000044;
                border-radius: 10px;
                border: 0.2px solid #ffffff50;

                .year {
                    position: absolute;
                    width: 100%;
                    top: 8px;
                    left: 0;
                    color: white;
                    font-size: 13px;
                    text-align: center;
                }

                .content-item {
                    position: absolute;
                    left: -62px;
                    bottom: 65px;
                    height: 95px;
                    width: 200px;
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
                    transform: rotate(-90deg);

                    .-item-title {
                        font-weight: bold;
                        margin-top: 12px;
                        font-size: 1.5rem;
                        cursor: default;
                        text-transform: uppercase;
                        color: #ffa200;
                        max-width: 150px;
                    }

                    .-item-name {
                        margin-top: 7px;
                        cursor: default;
                        text-transform: lowercase;
                        color: #ffffffdd;
                        font-size: 0.8rem;
                    }
                }
            }

        }
    }

    .verti-section::-webkit-scrollbar {
        width: 0 !important;
        height: 15px;
        background: #ffffff20;
        border-radius: 5px;
    }
}
</style>