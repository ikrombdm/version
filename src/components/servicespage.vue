<template>
    <section>

        <h1 class="all-title1">Services</h1>

        <div class="service-items">
            <div class="service-item">
                <div class="item-image">
                    <img :src="front" alt="">
                </div>
                <div class="item-content">
                    <h1>Front-end</h1>
                    <span>developer</span>
                </div>
            </div>
            <div class="service-item">
                <div class="item-image">
                    <img :src="back" alt="">
                </div>
                <div class="item-content">
                    <h1>Back-end</h1>
                    <span>developer</span>
                </div>
            </div>
            <div class="service-item">
                <div class="item-image">
                    <img :src="uiux" alt="">
                </div>
                <div class="item-content">
                    <h1>UI/UX</h1>
                    <span>designs</span>
                </div>
            </div>
            <div class="service-item">
                <div class="item-image">
                    <img :src="uiux" alt="">
                </div>
                <div class="item-content">
                    <h1>UI/UX</h1>
                    <span>designs</span>
                </div>
            </div>

        </div>

    </section>
</template>

<script>
import front from "@/assets/front.png"
import back from "@/assets/back.png"
import uiux from "@/assets/uiux.png"
export default {
    data() {
        return {
            front,
            back,
            uiux
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
    margin-top: 5rem;


    .service-items {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 2rem;
        padding: 2rem;

        .service-item {
            height: 80px;
            width: 265px;
            display: flex;
            align-items: center;
            gap: 1rem;
            border: 3px solid #ffffff49;
            padding: 10px;
            border-radius: 10px;



            .item-image {
                width: 60px;
                height: 60px;
                background: #ffa200;
                padding: 10px;
                border-radius: 5px;
                display: flex;
                justify-content: center;
                align-items: center;

                img {
                    width: 100%;
                    -webkit-user-drag: none !important;
                }
            }

            .item-content {
                h1 {
                    color: #ffa200;
                    font-size: 1.6rem;
                    text-transform: uppercase;
                    margin-bottom: 5px;
                }

                span {
                    color: #fff;
                    font-size: 1.1fr;
                }
            }
        }
    }
}
</style>