<template>
    <section class="mx-w">
        
        <div class="verti-section">

            <div class="verti-main">
                <div class="verti-item">
                    <p class="year">2023-2023</p>
                    <div class="content-item">
                        <div class="-item-title">School</div>
                        <div class="-item-name">Include collage</div>
                    </div>
                </div>

            </div>

        </div>

    </section>
</template>

<script>


</script>


<style lang="scss">
.verti-section {
    .verti-main {
        display: flex;
        gap: 1.5rem;
        overflow: scroll;

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
                top: -6px;
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
                    margin-top: 15px;
                    font-size: 1.3rem;
                    cursor: default;
                    text-transform: uppercase;
                    color: white;
                    max-width: 150px;
                }

                .-item-name {
                    margin-top: 5px;
                    cursor: default;
                    text-transform: lowercase;
                    color: #ffffff80;
                    font-size: 0.8rem;
                }
            }
        }

    }

    .verti-main::-webkit-scrollbar {
        display: none !important;
    }
}




.services-title {
    color: #ffffffb4;
    font-size: .9rem;
    margin-bottom: 1.4rem;
    text-transform: uppercase;
}

.services-section {
    display: flex;
    justify-content: space-between;
    gap: 5rem;
    margin-bottom: 10rem;


    .services {
        width: 100%;
        padding: 2.5rem;
        display: flex;
        flex-direction: column;
        align-items: center;
        background: #00000022;
        border-radius: 15px;

        svg {
            width: 40px;
            color: #cdd5e0ee;
        }

        h1 {
            margin-top: 1.8rem;
            color: #a8b3c2ee;
            font-size: 1rem;
            text-align: center;
        }
    }
}



.block {
    height: 80vh;
    display: grid;
    align-items: center;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;

    .main-left {
        color: #eee;

        p {
            line-height: 27px;
            margin-bottom: 28px;
        }

        a {
            color: #eee;
            border-radius: 10px;
        }

        a:hover {
            color: #00feba;
        }
    }

    .main-right {
        height: 150px;
        width: 150px;
        background: #eee;
        margin: 0 auto;
        border-radius: 50%;
    }
}
</style>