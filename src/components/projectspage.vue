<template>
    <section id="projects" class="mx-w">

        <h1 class="all-title2">Projects</h1>


        <div class="projects-section">

            <div class="project">


                <div class="project-item" v-for="project in projects" :key="project.id">
                    <div>
                        <div class="item-left">
                            <div id="item-header">
                                <a :href="project.link_demo" target="_blank" class="item-icon">
                                    <i class="fa-brands fa-github"></i>
                                    <i class="fa-solid fa-arrow-up-right-from-square"></i>
                                </a>
                                <h1 class="item-title">
                                    <a :href="project.link_live" target="_blank">
                                        {{ project.title }}
                                    </a>
                                </h1>
                            </div>

                            <div class="item-year-middle">{{ project.year }}</div>

                            <p class="item-content">
                                {{ project.content }}
                            </p>


                        </div>
                        <div class="item-right">
                            <img :src="project.image" :alt="project.title">
                        </div>
                    </div>
                </div>


            </div>
        </div>

    </section>
</template>

<script>

export default {
    data() {
        return {
            projects: [
                {
                    title: "Amodent",
                    content: "lorem",
                    year: 2023,
                    image: "https://static.wixstatic.com/media/ea6ac8_b6b0cbe25615488e855f515846354dda~mv2.jpg/v1/fill/w_640,h_420,al_c,q_80,usm_0.66_1.00_0.01,enc_auto/ea6ac8_b6b0cbe25615488e855f515846354dda~mv2.jpg",
                    link_live: "https://amodent.uz/",
                    link_demo: "https://amodent.uz/",
                },
            ]
        }
    }
}
</script>


<style lang="scss" scoped>
section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center !important;
    margin: 0 auto;
    gap: 1rem;
    -webkit-font-smoothing: antialiased;
    padding: 20px;

    .projects-section {
        margin-top: 4rem;

        .project-title {
            margin-top: 5rem;
            font-size: 1.2rem;
            color: #eeeeeebb;
            padding-bottom: 2rem;

            span {
                color: #ffa200;
            }
        }

        .project {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;



            .project-item {
                position: relative;
                background: #000000;
                width: 320px;
                min-height: 90px;
                justify-content: space-between;
                padding: 1rem 1rem 1rem 1.1rem;
                border: 2px solid #eeeeeead;
                border-radius: 15px;
                overflow: hidden;

                .item-left {
                    position: relative;
                    z-index: 99 !important;

                    #item-header {
                        display: flex !important;
                        align-items: center;
                        gap: 1rem;
                        text-decoration: none;

                        .item-icon {
                            width: 35px;
                            height: 35px;
                            background: #ffa200;
                            display: flex;
                            justify-content: center;
                            align-items: center;
                            color: #000;
                            border-radius: 8px;
                            text-decoration: none !important;


                        }

                        i {
                            position: absolute;
                            transition: 0.2s;
                        }

                        i:nth-child(2) {
                            opacity: 0;
                        }

                        .item-icon:hover i:nth-child(2) {
                            opacity: 1;
                        }

                        .item-icon:hover i:nth-child(1) {
                            opacity: 0;
                        }

                        .item-title {
                            position: relative;
                            font-size: 1.5rem;
                            color: #ddd;
                            text-transform: uppercase;
                            transition: .2s ease-in;

                            a {
                                color: #fff;
                                text-decoration: none;
                            }
                        }

                        .item-title:hover a {
                            color: #000;
                            transition: .2s ease;
                        }

                        .item-title::after {
                            position: absolute;
                            content: "";
                            left: -3%;
                            bottom: -1px;
                            height: 0px;
                            width: 105%;
                            background: #888;
                            z-index: -1;
                            transition: 0.2s ease-out;
                        }

                        .item-title:hover::after {
                            height: 115%;
                            background: #fff;

                        }
                    }



                    #item-header:hover {
                        color: #000;
                    }

                    #item-header:hover {
                        color: #000;
                    }

                    .item-year-middle {
                        position: absolute;
                        top: 20px;
                        left: 0px;
                        font-size: 3rem;
                        color: #ffffff33;
                        font-weight: bold;
                        z-index: -1;
                        text-align: center;
                    }


                    .item-content {
                        margin-top: 8px;
                        height: 65%;
                        color: #cdd3d8;
                        // overflow: scroll;
                        width: 100%;
                        max-width: 280px;
                        font-size: 15px;
                        line-height: 21px;

                        a {
                            color: #00ff9c;
                            padding: 0 2px 0 0;
                            transition: .2s ease;

                            i {
                                margin-left: 3px;
                                font-size: 10px;
                                color: #000;
                                opacity: 0;
                                transition: .2s ease;
                            }
                        }

                        a:hover {
                            background: #fff;
                            color: #000;
                        }

                        a:hover i {
                            opacity: 1;
                        }
                    }

                    .item-content::-webkit-scrollbar {
                        width: 0;
                        height: 0;
                    }

                }

                .item-right {
                    position: absolute;
                    right: 0%;
                    top: 0%;
                    width: 50%;
                    height: 100%;
                    border-radius: 10px;
                    overflow: hidden;
                }

                .item-right::after {
                    position: absolute;
                    content: "";
                    background: linear-gradient(90deg, #000000, #0000005e, transparent);
                    left: 0;
                    top: 0;
                    width: 200%;
                    height: 100%;
                }

                .item-right {
                    img {
                        height: 100%;
                        object-fit: cover;
                    }

                }

                .item-right:hover {
                    cursor: zoom-in;
                }
            }

        }

    }

}
</style>